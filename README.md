# Kinergize

App for managing your workouts.

## Goals
&nbsp;&nbsp;&nbsp;&nbsp; *The goal is to track various aspects of the workouts, so to have control and make potential improvements, e.g.:*

- 
- Days done/left till end of current plan, ex. 1/4 (3 left)

- Weight change:
  - since last 7 days, ex. +0.4kg, was 72.2kg, now 72.6kg
  - since last 14 days
  - since last 21 days
  - since last 28 days
  - since last week, ex. now is april 14th Friday... so compare to last Sunday - April 9th
  - since last month, ex. now is april 14th... so compare to March 31th

- Cm Measures of body parts:
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

- Sessions done count:
  - since current plan started, ex. current plan has 4 days, it started April 14th, now is April 16th, however you skept a session yesterday, so it is still 1 now, after doing todays session it will 2, or maybe you do two at once, so it will be 3?
  - since last 7 days, ex. 4 
  - since last 14 days
  - since last 21 days, ex. 18 (average 3 per plan, 2.3 per week)
  - since last 28 days
  - since last x days
  - since last month
  - since last 3 months
  - since last 6 months
  - since last 12 months
  - since last year
  - since last 2 years (or x years)
  
 - Exercises done:
  - since current plan started, ex. 56/87 (31 left),
  - since last 7 days, ex. 241, (average since 1before - 48 per session actually done, 31 per day in general)
  - since last x days, ex. 241,
  - since last 10 weeks, ex. 2024 (average since then - 38 per session, 31 per day in general, 102 per week in general)
  
 - Sessions durations and changes:
   - average since current plan started, ex. 33m 23s (+ 3m 4s since last session)
   - average since last 2 sessions - current + last, etc.
   - average since last x sessions
   - average since last 7 days
   - average since last 14 days, etc.
   - ...

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

- Sleep hours:
  - ??

- Has the plans has been done as expected, have some days been skept, or plans done over the whole day or missing exercises, maybe done two session in same day??
- How warm-ups has been done before workouts - how many minutes..
- How many exercises I've done last week, weeks or months or year(s)
- How many exercises I've done last week, weeks or months or year(s) PER MUSCLE GROUP
- How many days I skept while doing a plan - diagram, corellation with sleep, general feeling while doing exercises
- How much time I spent on exercises given day, last week, weeks or months or year(s)
- How exercise time changed over last times, ex. last 
- How many exercises do I have left till the end of current day, plan, week, month, etc.
- How well I felt doing my exercises.. last week... - diagram corellation with sleep, or series amount, or intensity...
- How my biometrics changed over time last week, weeks or months or year(s) (weight, cms) - diagram corellation with wellness, or series amount, or intensity

## API - User

### Biometrics
| HTTP Method | Endpoint | Description | Details |
| --- | --- | --- | --- |
| `GET` | `api/me/biometrics` | Get own biometrics details | [link]() |
| `PUT` | `api/me/biometrics` | Update own biometrics details | [link]() |

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
