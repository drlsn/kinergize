
## Roles

ADMIN > USER

## Endpoints

### Workout Programs - user?
| HTTP Method | Endpoint | Short Description | Role |
| --- | --- | --- | --- |
| `POST` | `api/users/{userId}/programs` | Create a workout program | USER |
| `GET` | `api/users/{userId}/programs` | Get workout programs list | USER |
| `GET` | `api/users/{userId}/programs/{programId}` | Get a workout program details | USER |
| `PUT` | `api/users/{userId}/programs/{programId}` | Update a workout program details | USER |
| `DELETE` | `api/users/{userId}/programs/{programId}` | Delete a workout program | USER |

### Exercises - admin?
| HTTP Method | Endpoint | Short Description | Role |
| --- | --- | --- | --- |
| `POST` | `api/exercises` | Create an exercise | ADMIN |
| `GET` | `api/exercises` | Get exercises list | USER |
| `GET` | `api/exercises/{exerciseId}` | Get an exercise details | USER |
| `PUT` | `api/exercises/{exerciseId}` | Update an exercise details | ADMIN |
| `DELETE` | `api/exercises/{exerciseId}` | Delete an exercise | ADMIN |
