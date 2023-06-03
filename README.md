# Kinergize

App for managing your workouts

## API - User

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
| `PATCH` | `api/me/sessions/{sessionId}` | Modify or end the workout session | [link]() |

### Workout Session Exercises
| HTTP Method | Endpoint | Short Description | Details |
| --- | --- | --- | --- |
| `POST` | `api/me/sessions/{sessionId}/exercises` | Start an exercise of the workout session | [link]() |
| `PUT` | `api/me/sessions/{sessionId}/exercises/{exerciseId}` | Modify the exercise details | [link]() |

### Workout Sessions Statistics
| HTTP Method | Endpoint | Short Description | Details |
| --- | --- | --- | --- |
| `GET` | `api/me/statistics` | Start an exercise of the workout session | [link]() |

## API - Admin
