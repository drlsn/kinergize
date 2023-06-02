TO DO: a file per endpoint?

## Roles

ADMIN > USER

## Endpoints

### Workout Programs - admin?
| HTTP Method | Endpoint | Short Description | Role |
| --- | --- | --- | --- |
| `POST` | `api/users/{userId}/programs` | Create a workout program | USER |
| `GET` | `api/users/{userId}/programs` | Get workout programs list | USER |
| `GET` | `api/users/{userId}/programs/{programId}` | Get a workout program details | USER |
| `PUT` | `api/users/{userId}/programs/{programId}` | Update a workout program details | USER |
| `DELETE` | `api/users/{userId}/programs/{programId}` | Delete a workout program | USER |

### Workout Programs - user?
| HTTP Method | Endpoint | Short Description | Role |
| --- | --- | --- | --- |
| `POST` | `api/me/programs` | Create a workout program | ADMIN |
| `GET` | `api/me/programs` | Get workout programs list | ADMIN |
| `GET` | `api/me/programs/{programId}` | Get a workout program details | ADMIN |
| `PUT` | `api/me/programs/{programId}` | Update a workout program details | ADMIN |
| `DELETE` | `api/users/{userId}/programs/{programId}` | Delete a workout program | ADMIN |

### Exercises - admin?
| HTTP Method | Endpoint | Short Description | Role | Long Description |
| --- | --- | --- | --- | --- |
| `POST` | `api/exercises` | Create an exercise | ADMIN | Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500 |
| `GET` | `api/exercises` | Get exercises list | USER |
| `GET` | `api/exercises/{exerciseId}` | Get an exercise details | USER |
| `PUT` | `api/exercises/{exerciseId}` | Update an exercise details | ADMIN |
| `DELETE` | `api/exercises/{exerciseId}` | Delete an exercise | ADMIN |
