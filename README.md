# Kinergize

App for managing your workouts.

## Goals
&nbsp;&nbsp;&nbsp;&nbsp; *The goal is to track various aspects of the workouts, so to have control and make potential improvements, e.g.:*

- Days done/left till end of current plan, ex. 1/4 (3 left)

- Biometrics - Weight:
  - since last 7 days, ex. +0.4kg, was 72.2kg, now 72.6kg (average since then, 72.4kg?)
  - since last 14 days
  - since last 21 days
  - since last 28 days
  - since last week, ex. now is april 14th Friday... so compare to last Sunday - April 9th
  - since last month, ex. now is april 14th... so compare to March 31th

- Biometrics - cm measures of body parts:
  - since last 7 days, ex. biceps +1cm, chest +1cm, was 40cm, now 41cm,
  - since last 14 days
  - since last 21 days
  - since last 28 days
  - since last x days (to be selectable from dropdown or put to text field)
  - since last month
  - since last 3 months (or n months, to be selectable from dropdown or put to text field)
  - since last 6 months
  - since last 12 months, ex. now is april 14th 2023... so compare to April 14th 2022
  - since last year, ex. now is april 14th 2023... so compare to December 31th 2022
  - since last 2 years (or x years)

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
  
- Exercises - All:
  - since current plan started, ex. 56/87 (31 left),
  - since last 7 days, ex. 241, + average since 1before - 48 per session actually done, 31 per day in general)
  - since last x days, ex. 241,
  - since last 10 weeks, ex. 2024 (average since then - 38 per session, 31 per day in general, 102 per week in general)
 
 - Exercises durations and changes:
   - chest exercises:
     - dumbbell press:
       - now vs the 1 before, ex. 38s now / 42s 1before (average since 1before - 40s)
       - now vs the 2 before (or x before), ex. 38s now / 44s 2before (average since 2before - 42s)
       - etc. 7 days, weeks, months and so on ...
     - exercise x.. and so on...
   - back exercises.. and so on..
     - ...
       - ...
   - ...

- Exercises:
  - All
  - Per Muscle Group
    - chest:
      - reps done since current plan started per muscle group, ex. 23 done / 26 planned
      - reps done since 2 or x plans ex. 45 done / 53 planned / 8 skept
      - reps done since x days, weeks, so on

  - Per Exercise
   - chest exercises:
     - dumbbell press (able to switch between "by time" or "by info type"):
       - reps done since current plan started per muscle group, ex. 23 done / 26 planned
       - reps done since 2 or x plans ex. 45 done / 53 planned / 8 skept
       - reps done since x days, weeks, so on
       - now vs the 1 before, ex. 38s now / 42s 1before (average since 1before - 40s)
       - now vs the 2 before (or x before), ex. 38s now / 44s 2before (average since 2before - 42s)
       - etc. 7 days, weeks, months and so on ...
     - exercise x.. and so on...
   - back exercises.. and so on..

## API - User

### Biometrics
| HTTP Method | Endpoint | Description | Details |
| --- | --- | --- | --- |
| `GET` | `api/me/biometrics` | Get own biometrics details | [link]() |
| `PUT` | `api/me/biometrics` | Update own biometrics details | [link]() |

### Biometrics - Weight
| `POST` | `api/me/biometrics/weights` | Add weight biometric | [link]() |
| `POST` | `api/me/biometrics/measures` | Add measure biometric | [link]() |
| `GET` | `api/me/biometrics/measures` | Add measure biometric | [link]() |

### Workout Plans
| HTTP Method | Endpoint | Description | Details |
| --- | --- | --- | --- |
| `POST` | `api/me/programs` | Create own workout program | [link]() |
| `GET` | `api/me/programs` | Get own workout programs list | [link]() |
| `GET` | `api/me/programs/{programId}` | Get own workout program details | [link]() |
| `PUT` | `api/me/programs/{programId}` | Update own workout program details | [link]() |
| `DELETE` | `api/me/programs/{programId}` | Delete own workout program | [link]() |
.. also cancel current doing plan - meaning start over

### Exercises
| HTTP Method | Endpoint | Short Description | Details |
| --- | --- | --- | --- |
| `POST` | `api/me/exercises` | Create own exercise | [link](docs/API/User/Exercises/Create%20own%20Exercise.md) |
| `GET` | `api/me/exercises` | Get own exercises list | [link]() |
| `GET` | `api/me/exercises/{exerciseId}` | Get own exercise details | [link]() |
| `PUT` | `api/me/exercises/{exerciseId}` | Update own exercise details | [link]() |
| `DELETE` | `api/me/exercises/{exerciseId}` | Delete own exercise | [link]() |

### Workout Program Exercises
| HTTP Method | Endpoint | Short Description | Details |
| --- | --- | --- | --- |
| `GET` | `api/me/programs/{programId}/exercises` | Get all exercises of the workout program | [link]() |
| `GET` | `api/me/programs/{programId}/days/{dayIndex}/exercises` | Get all exercises of the workout program's single day | [link]() |

### Workout Sessions
| HTTP Method | Endpoint | Short Description | Details |
| --- | --- | --- | --- |
| `POST` | `api/me/sessions/{sessionId}` | Start a workout session | [link]() |
| `PATCH` | `api/me/sessions/{sessionId}` | Update or end the workout session | [link]() |

### Workout Session Exercises
| HTTP Method | Endpoint | Short Description | Details |
| --- | --- | --- | --- |
| `POST` | `api/me/sessions/{sessionId}/exercises` | Start an exercise of the workout session | [link]() |
| `PUT` | `api/me/sessions/{sessionId}/exercises/{exerciseId}` | Modify the exercise details | [link]() |

### Statistics
| HTTP Method | Endpoint | Short Description | Details |
| --- | --- | --- | --- |
| `GET` | `api/me/statistics` | Get statistics about workouts | [link](/docs/API/User/Statistics/Get%20Workouts%20Statistics.md) |

## API - Admin


## Glossary

#### Repetition

#### Workout

#### Plan

#### Exercise

#### Muscle Group
