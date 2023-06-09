# Kinergize

[1. General](#general)  
[2. API](#api)  
[3. Architecture](#architecture)  
[4. UI Design](#ui-design)  
&nbsp;&nbsp;&nbsp;&nbsp;[4.1 View Descriptions](#view-content-analisys)  
&nbsp;&nbsp;&nbsp;&nbsp;[4.2 Mockups](#mockups)  

## General

&nbsp;&nbsp;&nbsp;&nbsp; App for adding and tracking progress of your workouts, so to make potential improvements in the future.

#### Tech
&nbsp;&nbsp;&nbsp;&nbsp; HTML, CSS, C#, Blazor Server, .NET, AWS, Docker

#### Demo Urls
&nbsp;&nbsp;&nbsp;&nbsp; http://kinergize.me  
&nbsp;&nbsp;&nbsp;&nbsp; http://kinergize.com  
&nbsp;&nbsp;&nbsp;&nbsp; http://kinergize.pl  

#### Implementation
&nbsp;&nbsp;&nbsp;&nbsp; Since the implementation will serve as fundament for future projects, for now it is located at:
- https://github.com/drlsn/Corelibs.Blazor.UIComponents
- https://github.com/drlsn/blazor-app-template

&nbsp;&nbsp;&nbsp;&nbsp; It will be copied here at some point.

## API

The API is inspired mainly by [SpotifyAPI](https://developer.spotify.com/documentation/web-api). 

Every endpoint requires at least a certain role to be able to execute it successfully. Depending on a role the same endpoint might return different amounts of data. The roles, from the most to the least privileged, are:
- Admin - requires an authorization token with the role assigned
- User - requires an authorization token
- Guest - does not require any authorization token

More information about the API can be found in [Kinergize - API General Info](/docs/API/Kinergize%20-%20API%20General%20Info.md) document.

### Users
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/users` | Get all users | Admin | [link](/docs/API/Users/Get%20all%20users.md) |
| `GET` | `api/users/{userId}` | Get the user details | Admin | [link](/docs/API/Users/Get%20the%20user%20details.md) |
| `POST` | `api/users` | Add a user | User | [link](/docs/API/Users/Add%20a%20user.md) |
| `GET` | `api/me` | Get the user details - own | User | [link](/docs/API/Users/Get%20the%20user%20details%20-%20own.md) |
| `PUT` | `api/me` | Update the user details | User | [link](/docs/API/Users/Update%20the%20user%20details.md) |

### Workout Plans
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/plans` | Get all workout plans | Admin | [link](/docs/API/Workout%20Plans/Get%20all%20workout%20plans.md) |
| `GET` | `api/plans/me` | Get all workout plans - own | User | [link](/docs/API/Workout%20Plans/Get%20all%20workout%20plans%20-%20own.md) |
| `POST` | `api/plans/me` | Add a workout plan - own, private | User | [link](/docs/API/Workout%20Plans/Add%20a%20workout%20plan%20-%20own,%20private.md) |
| `GET` | `api/plans/public` | Get all workout plans - public | Guest | [link](/docs/API/Workout%20Plans/Get%20all%20workout%20plans%20-%20public.md) |
| `POST` | `api/plans/public` | Add a workout plan as public | Admin | [link](/docs/API/Workout%20Plans/Add%20a%20workout%20plan%20as%20public.md) |
| `GET` | `api/plans/private` | Get all workout plans - private | Admin | [link](/docs/API/Workout%20Plans/Get%20all%20workout%20plans%20-%20private.md) |
| `GET` | `api/plans/{planId}` | Get the workout plan details | Guest | [link](/docs/API/Workout%20Plans/Get%20the%20workout%20plan%20details.md) |
| `PUT` | `api/plans/{planId}` | Update the workout plan details | User | [link](/docs/API/Workout%20Plans/Update%20the%20workout%20plan%20details.md) |
| `DELETE` | `api/plans/{planId}` | Delete the workout plan | User | [link](/docs/API/Workout%20Plans/Delete%20the%20workout%20plan.md) |

### Workout Plan Aims
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/plans/aims` | Get all workout plan aims | Admin | [link](/docs/API/Workout%20Plans%20Aims/Get%20all%20workout%20plan%20aims.md) |
| `GET` | `api/plans/aims/public` | Get all workout plan aims - public | Admin | [link](/docs/API/Workout%20Plans%20Aims/Get%20all%20workout%20plan%20aims%20-%20public.md) |
| `GET` | `api/plans/aims/private` | Get all workout plan aims - private | Admin | [link](/docs/API/Workout%20Plans%20Aims/Get%20all%20workout%20plan%20aims%20-%20private.md) |
| `GET` | `api/plans/aims/me` | Get all workout plan aims - own | User | [link](/docs/API/Workout%20Plans%20Aims/Get%20all%20workout%20plan%20aims%20-%20own.md) |
| `GET` | `api/plans/{planId}/aims` | Get all workout plan aims - specific plan | User | [link](/docs/API/Workout%20Plans%20Aims/Get%20all%20workout%20plan%20aims%20-%20specific%20plan.md) |
| `GET` | `api/plans/{planId}/aims/public` | Get all workout plan aims - specific plan, public | Admin | [link](/docs/API/Workout%20Plans%20Aims/Get%20all%20workout%20plan%20aims%20-%20specific%20plan,%20public.md) |
| `GET` | `api/plans/{planId}/aims/private` | Get all workout plan aims - specific plan, private | Admin | [link](/docs/API/Workout%20Plans%20Aims/Get%20all%20workout%20plan%20aims%20-%20specific%20plan,%20private.md) |
| `POST` | `api/plans/{planId}/aims` | Start a workout plan aim | Admin | [link](/docs/API/Workout%20Plans%20Aims/Start%20a%20workout%20plan%20aim.md) |
| `GET` | `api/plans/aims/{aimId}` | Get the workout plan aim details | User | [link](/docs/API/Workout%20Plans%20Aims/Get%20the%20workout%20plan%20aim%20details.md) |
| `PUT` | `api/plans/aims/{aimId}` | Update the workout plan aim details | User | [link](/docs/API/Workout%20Plans%20Aims/Update%20the%20workout%20plan%20aim%20details.md) |
| `DELETE` | `api/plans/aims/{aimId}` | Finish the workout plan aim | User | [link](/docs/API/Workout%20Plans%20Aims/Finish%20the%20workout%20plan%20aim.md) |

### Sessions
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/sessions` | Get all sessions | Admin | [link](/docs/API/Sessions/Get%20all%20sessions.md) |
| `GET` | `api/sessions/me` | Get a session list - own | User | [link](/docs/API/Sessions/Get%20a%20session%20list%20-%20own.md) |
| `POST` | `api/sessions/me` | Add a session - own, private | User | [link](/docs/API/Sessions/Add%20a%20session%20-%20own,%20private.md) |
| `GET` | `api/sessions/public` | Get all sessions - public | Guest | [link](/docs/API/Sessions/Get%20all%20sessions%20-%20public.md) |
| `POST` | `api/sessions/public` | Add a session as public | Admin | [link](/docs/API/Sessions/Add%20a%20session%20as%20public.md) |
| `GET` | `api/sessions/private` | Get all sessions - private | Admin | [link](/docs/API/Sessions/Get%20all%20sessions%20-%20private.md) |
| `GET` | `api/sessions/{sessionId}` | Get the session details | User | [link](/docs/API/Sessions/Get%20the%20session%20details.md) |
| `PUT` | `api/sessions/{sessionId}` | Update the sessions details | User | [link](/docs/API/Sessions/Update%20the%20sessions%20details.md) |
| `DELETE` | `api/sessions/{sessionId}` | Delete the session | User | [link](/docs/API/Sessions/Delete%20the%20session.md) |

| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/plans/{planId}/sessions` | Get sessions list of the workout plan | Guest | [link](/docs/API/Sessions/Get%20sessions%20list%20of%20the%20workout%20plan.md) |
| `POST` | `api/plans/{planId}/sessions` | Add a session to the workout plan | User | [link](/docs/API/Sessions/Add%20a%20session%20to%20the%20workout%20plan.md) |
| `DELETE` | `api/plans/{planId}/sessions/{sessionId}` | Remove a session from the workout plan | User | [link](/docs/API/Sessions/Remove%20a%20session%20from%20the%20workout%20plan.md) |

### Session Aims
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/sessions/{sessionId}/aims` | Get all session aims | Admin | [link](/docs/API/Sessions%20Aims/Get%20all%20session%20aims.md) |
| `GET` | `api/sessions/{sessionId}/aims/public` | Get all session aims - public | Admin | [link](/docs/API/Sessions%20Aims/Get%20all%20session%20aims%20-%20public.md) |
| `GET` | `api/sessions/{sessionId}/aims/private` | Get all session aims - private | Admin | [link](/docs/API/Sessions%20Aims/Get%20all%20session%20aims%20-%20private.md) |
| `GET` | `api/sessions/aims/me` | Get all session aims - own | User | [link](/docs/API/Sessions%20Aims/Get%20all%20session%20aims%20-%20own.md) |
| `POST` | `api/sessions/{sessionId}/aims` | Start a session aim | Admin | [link](/docs/API/Sessions%20Aims/Start%20a%20session%20aim.md) |
| `GET` | `api/sessions/aims/{aimId}` | Get the session aim details | User | [link](/docs/API/Sessions%20Aims/Get%20the%20session%20aim%20details.md) |
| `PUT` | `api/sessions/aims/{aimId}` | Update the session aim details | User | [link](/docs/API/Sessions%20Aims/Update%20the%20session%20aim%20details.md) |
| `DELETE` | `api/sessions/aims/{aimId}` | Finish the session aim | User | [link](/docs/API/Sessions%20Aims/Finish%20the%20session%20aim.md) |

### Exercises
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/exercises` | Get all exercises | Admin | [link](/docs/API/Exercises/Get%20all%20exercises.md) |
| `GET` | `api/exercises/me/` | Get exercises list - own | User | [link](/docs/API/Exercises/Get%20exercises%20list%20-%20own.md) |
| `POST` | `api/exercises/me/` | Add an exercise - own, private | User | [link](docs/API/Exercises/Add%20an%20exercise%20-%20own,%20private.md) |
| `GET` | `api/exercises/public` | Get all exercises - public only | Guest | [link](/docs/API/Exercises/Get%20all%20exercises%20-%20public%20only.md) |
| `POST` | `api/exercises/public` | Add an exercise as public | Admin | [link](/docs/API/Exercises/Add%20an%20exercise%20as%20public.md) |
| `GET` | `api/exercises/private` | Get all exercises - private only | Admin | [link](/docs/API/Exercises/Get%20all%20exercises%20-%20private%20only.md) |
| `GET` | `api/exercises/{exerciseId}` | Get the exercise details | User | [link](/docs/API/Exercises/Get%20the%20exercise%20details.md) |
| `PUT` | `api/exercises/{exerciseId}` | Update the exercise details | User | [link](/docs/API/Exercises/Update%20the%20exercise%20details.md) |
| `DELETE` | `api/exercises/{exerciseId}` | Delete the exercise | User | [link](/docs/API/Exercises/Delete%20the%20exercise.md) |

| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/plans/{planId}/exercises` | Get the workout plan exercises list | Guest | [link](/docs/API/Exercises/Get%20the%20workout%20plan%20exercises%20list.md) |

### Exercise Aims
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/exercises/{exerciseId}/aims` | Get all exercise aims | Admin | [link](/docs/API/Exercises%20Aims/Get%20all%20exercise%20aims.md) |
| `GET` | `api/exercises/{exerciseId}/aims/public` | Get all exercise aims - public | Admin | [link](/docs/API/Exercises%20Aims/Get%20all%20exercise%20aims%20-%20public.md) |
| `GET` | `api/exercises/{exerciseId}/aims/private` | Get all exercise aims - private | Admin | [link](/docs/API/Exercises%20Aims/Get%20all%20exercise%20aims%20-%20private.md) |
| `GET` | `api/exercises/aims/me` | Get all exercise aims - own | User | [link](/docs/API/Exercises%20Aims/Get%20all%20exercise%20aims%20-%20own.md) |
| `POST` | `api/exercises/{exerciseId}/aims` | Start an exercise aim | Admin | [link](/docs/API/Exercises%20Aims/Start%20an%20exercise%20aim.md) |
| `GET` | `api/exercises/aims/{aimId}` | Get the exercise aim details | User | [link](/docs/API/Exercises%20Aims/Get%20the%20exercise%20aim%20details.md) |
| `PUT` | `api/exercises/aims/{aimId}` | Update the exercise aim details | User | [link](/docs/API/Exercises%20Aims/Update%20the%20exercise%20aim%20details.md) |
| `DELETE` | `api/exercises/aims/{aimId}` | Finish the exercise aim | User | [link](/docs/API/Exercises%20Aims/Finish%20the%20exercise%20aim.md) |

| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `POST` | `api/sessions/aims/{sessionAimId}/exercises/{exerciseId}/aims` | Start an exercise aim of a session | User | [link](/docs/API/Exercises%20Aims/Start%20an%20exercise%20aim%20of%20a%20session.md) |
| `DELETE` | `api/sessions/aims/{sessionAimId}/exercises/{exerciseId}/aims/{exerciseAimId}` | Finish an exercise aim of a session | User | [link](/docs/API/Exercises%20Aims/Finish%20an%20exercise%20aim%20of%20a%20session.md) |

### Statistics
| HTTP Method | Endpoint | Short Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/statistics/me` | Get statistics about workouts | User | [link](/docs/API/Statistics/Get%20statistics%20about%20workouts.md) |
| `GET` | `api/statistics/me/plans` | Get statistics about done workout plans | User | [link](/docs/API/Statistics/Get%20statistics%20about%20done%20workout%20plans.md) |
| `GET` | `api/statistics/me/sessions` | Get statistics about done sessions | User | [link](/docs/API/Statistics/Get%20statistics%20about%20done%20sessions.md) |
| `GET` | `api/statistics/me/exercises` | Get statistics about done exercises | User | [link](/docs/API/Statistics/Get%20statistics%20about%20done%20exercises.md) |
| `GET` | `api/statistics/me/exercises?bodyPart={bodyPartName}` | Get statistics about done exercises per body part | User | [link](/docs/API/Statistics/Get%20statistics%20about%20done%20exercises%20per%20body%20part.md) |
| `GET` | `api/statistics/me/exercises?id={exerciseId}` | Get statistics about done exercises per type (id) | User | [link](/docs/API/Statistics/Get%20statistics%20about%20done%20exercises%20per%20type%20(id).md) |
| `GET` | `api/statistics/me/exercises?id={exerciseId}&created:gte:yyyy-mm-ddThh:mm:ss` | Get statistics about done exercises per type (id) since a date time | User | [link](/docs/API/Statistics/Get%20statistics%20about%20done%20exercises%20per%20type%20(id)%20since%20a%20date%20time.md) |

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

## Architecture

#### System Context - Level 0
![System Level Context Diagram](/docs/images/Architecture/Kinergize%20-%20System%20Level%20Context%20Diagram.png)

## UI Design

### View Content Analisys

#### Workout Plans

![Workout Plans UI Content](/docs/images/UI%20Content/Workout%20Plans.png)

#### Workout Plan Details

![Workout Plan Details UI Content](/docs/images/UI%20Content/Workout%20Plan%20Details.png)

#### Workout Statistics

##### Workout Plans

- Workout Plans - counts:
  - Days done/left till end of current plan, ex. 1/4 (3 left)
  - count since last 7 days, ex. 1
  - count since last 14 days, ex. 3 + average plan and per week
  - and so on..
- Workout Plans - durations:
  - duration of current plan

##### Sessions

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

##### Exercises
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

### Mockups

#### Homepage

![Homepage UI Design](/docs/images/UI%20Design/Kinergize%20-%20UI%20Design%20-%20Homepage.png)
