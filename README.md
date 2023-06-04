# Kinergize

&nbsp;&nbsp;&nbsp;&nbsp; App for adding and tracking progress of your workouts, so to make potential improvements in the future.

#### Tech
&nbsp;&nbsp;&nbsp;&nbsp; HTML, CSS, JavaScript, React.js, C#/.NET, AWS, Docker, WebApi

## API

The API is inspired mainly by [SpotifyAPI](https://developer.spotify.com/documentation/web-api). 

Every endpoint requires at least a certain role to be able to execute it successfully. Depending on a role the same endpoint my return different amounts of data. The roles, from the most to the least privileged, are:
- Admin
- User
- Guest - does not requires an authorization token

### Workout Plans - General
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/plans` | Get all workout plans - public and private | Admin | [link]() |
| `GET` | `api/plans/{planId}` | Get the workout plan details | User | [link]() |
| `PUT` | `api/plans/{planId}` | Update the workout plan details | User | [link]() |
| `DELETE` | `api/plans/{planId}` | Delete the workout plan | User | [link]() |
| `POST` | `api/plans/public` | Add a workout plan as public | Admin | [link]() |
| `GET` | `api/plans/public` | Get all workout plans - public only | Guest | [link]() |
| `GET` | `api/plans/private` | Get all workout plans - private only | Admin | [link]() |

### Workout Plans - Own
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `POST` | `api/me/plans` | Add own workout plan | User | [link]() |
| `GET` | `api/me/plans` | Get own private workout plan list | User | [link]() |

### Workout Plans - Operations
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `POST` | `api/me/plans/{planId}/start` | Start the workout plan | User | [link]() |
| `POST` | `api/me/plans/{planId}/finish` | Finish current workout plan | User | [link]() |

### Sessions - General
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/sessions` | Get all sessions - public and private | Admin | [link]() |
| `GET` | `api/sessions/{sessionId}` | Get the session details | User | [link]() |
| `PUT` | `api/sessions/{sessionId}` | Update the sessions details | User | [link]() |
| `DELETE` | `api/sessions/{sessionId}` | Delete the session | User | [link]() |
| `POST` | `api/sessions/public` | Add a session as public | Admin | [link]() |
| `GET` | `api/sessions/public` | Get all sessions - public only | Guest | [link]() |
| `GET` | `api/sessions/private` | Get all sessions - private only | Admin | [link]() |

### Sessions - Own
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `POST` | `api/me/sessions` | Add own private session | User | [link](docs/API/User/Exercises/Create%20own%20Exercise.md) |
| `GET` | `api/me/sessions` | Get own session list | User | [link]() |

### Sessions - By Workout Plan
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/plans/{planId}/sessions` | Get sessions list of the workout plan | Guest | [link]() |
| `POST` | `api/plans/{planId}/sessions` | Add a session to the workout plan | User | [link]() |
| `DELETE` | `api/plans/{planId}/sessions/{sessionId}` | Remove a session from the workout plan | User | [link]() |

### Sessions - Operations
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `POST` | `api/sessions/{sessionId}/start` | Start a workout session | User | [link]() |
| `POST` | `api/sessions/{sessionId}/finish` | Finish a workout session | User | [link]() |

### Exercises - General
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/exercises` | Get all exercises - public and private | Admin | [link]() |
| `GET` | `api/exercises/{exerciseId}` | Get the exercise details | User | [link]() |
| `PUT` | `api/exercises/{exerciseId}` | Update the exercise details | User | [link]() |
| `DELETE` | `api/exercises/{exerciseId}` | Delete the exercise | User | [link]() |
| `POST` | `api/exercises/public` | Add an exercise as public | Admin | [link]() |
| `GET` | `api/exercises/public` | Get all exercises - public only | Guest | [link]() |
| `GET` | `api/exercises/private` | Get all exercises - private only | Admin | [link]() |

### Exercises - Own
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `POST` | `api/me/exercises` | Add own private exercise | User | [link](docs/API/User/Exercises/Create%20own%20Exercise.md) |
| `GET` | `api/me/exercises` | Get own exercises list | User | [link]() |

### Exercises - By Workout Plan 
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/plans/{planId}/exercises` | Get workout plan exercises list | Guest | [link]() |

### Exercises - Operations
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `POST` | `api/sessions/{sessionId}/exercises/{exerciseId}/start` | Start the exercise | User | [link]() |
| `POST` | `api/sessions/{sessionId}/exercises/{exerciseId}/finish` | Finish the exercise | User | [link]() |
| `PUT` | `api/sessions/{sessionId}/exercises/{exerciseId}` | Update the exercise details | User | [link]() |

### Statistics
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/me/statistics` | Get statistics about workouts | User | [link](/docs/API/User/Statistics/Get%20Workouts%20Statistics.md) |
| `GET` | `api/me/statistics/plans` | Get statistics about done workout plans | User | [link]() |
| `GET` | `api/me/statistics/sessions` | Get statistics about done sessions | User | [link]() |
| `GET` | `api/me/statistics/exercises` | Get statistics about done exercises | User | [link]() |
| `GET` | `api/me/statistics/exercises?bodyPart={bodyPartName}` | Get statistics about done exercises per body part | User | [link]() |
| `GET` | `api/me/statistics/exercises?id={exerciseId}` | Get statistics about done exercises per type (id) | User | [link]() |
| `GET` | `api/me/statistics/exercises?id={exerciseId}&created:lte:2021-01-20T00:00:00` | Get statistics about done exercises per type (id) since a date time | User | [link]() |

## Concepts Description

- Each workout plan consists of multiple sessions.
- Each session consists of multiple sets.
- Each sets consists of multiple exercises.
- Each exercise consists of multiple reps.
- Each rep consists of multiple movements (most often two).

*In reality the movements of a rep could be more complex, but this is a general idea.*

Plan ➜ Session ➜ Set ➜ Exercise ➜ Rep ➜ Movement

- Each exercise can be done several times per session.
- Each exercise consists of several reps.
- A rep usually consists of two types of motions:
  - concentric - positive, lifting weight up - push up against gravity
  - eccentric - negative, lowering weight down - resisiting against gravity
- A rep might be done with various range of motions:
  - full - perfect
  - almost full - almost perfect or not sure
  - normal
  - half
  - other, but for noobs..
- A rep might be done with different speeds of motions:
  - Very slow
  - Slow
  - Normal
  - Fast
  - Very fast

- Each session is planned to be done on a certain day - 1st, 2nd, 3rd and so on. 
- Each session could be done earlier than planned or later.
- Current session could be done earlier than planned or later.
- Current workout plan, session, session can be canceled and started over or can be done over longer time span than planned.

## Views

### Workout Statistics

#### Workout Plans

- Workout Plans - counts:
  - Days done/left till end of current plan, ex. 1/4 (3 left)
  - count since last 7 days, ex. 1
  - count since last 14 days, ex. 3 + average plan and per week
  - and so on..
- Workout Plans - durations:
  - duration of current plan

#### Sessions

- Sessions - counts:
  - count since current plan started, ex. current plan has 4 days, it started April 14th, now is April 16th, however you skept a session yesterday, so it is still 1 now, after doing todays session it will 2, or maybe you do two at once, so it will be 3?
  - count since last 7 days, ex. 4 + average per day
  - count since last 14 days, ex. 4 + average per day, plan and per week
  - count since last 21 days, ex. 18 (average 3 per plan, 2.3 per week.. per day), 
  - count since last 28 days
  - count since last x days
  - count since last month
  - count since last 3 months
  - count since last 6 months
  - count since last 12 months
  - count since last year
  - count since last 2 years (or x years)
  - and so on..
  
- Sessions - durations:
   - duration since current plan started, ex. 1h 33m 23s (+ 3m 4s since last session), + average per day, per session
   - duration since last 2 sessions (current + last), ex. 4h 36m + average per day, per session, per plan
   - duration since last x sessions + average
   - duration since last 7 days + average
   - duration since last 14 days, + average 
   - and so on..

#### Exercises
- Exercises - All
  - since current plan started, ex. 56/87 (31 left),
  - since last 7 days, ex. 241, + average since 1before - 48 per session actually done, 31 per day in general)
  - since last x days, ex. 241,
  - since last 10 weeks, ex. 2024 (average since then - 38 per session, 31 per day in general, 102 per week in general) 

- Exercises - Per Body Part and Exercise
  - chest exercises:
    - dumbbell press (able to switch between "by time" or "by info type"?):
      - reps done since current plan started per muscle group, ex. 23 done / 26 planned
      - reps done since 2 or x plans ex. 45 done / 53 planned / 8 skept
      - reps done since x days, weeks, so on
      - duration now vs the 1 before, ex. 38s now / 42s 1before (average since 1before - 40s)
      - duration now vs the 2 before (or x before), ex. 38s now / 44s 2before (average since 2before - 42s)
      - etc. 7 days, weeks, months and so on ...
    - exercise x.. and so on...
 - back exercises.. and so on..
