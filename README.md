# Kinergize

App for managing your workouts.

## Goals
&nbsp;&nbsp;&nbsp;&nbsp; *The goal is to track various aspects of the workouts, so to have control and make potential improvements, e.g.:*

- How many sessions has been done since last week, n last weeks, months or year(s)
- Has the plans has been done as expected, have some days been skept, or plans done over the whole day or missing exercises
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

### Workout Programs
| HTTP Method | Endpoint | Description | Details |
| --- | --- | --- | --- |
| `POST` | `api/me/programs` | Create own workout program | [link]() |
| `GET` | `api/me/programs` | Get own workout programs list | [link]() |
| `GET` | `api/me/programs/{programId}` | Get own workout program details | [link]() |
| `PUT` | `api/me/programs/{programId}` | Update own workout program details | [link]() |
| `DELETE` | `api/me/programs/{programId}` | Delete own workout program | [link]() |

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
