
## Views
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

## API
| HTTP Method | Endpoint | Description | Details |
| --- | --- | --- | --- |
| `GET` | `api/me/biometrics` | Get own biometrics details | [link]() |
| `PUT` | `api/me/biometrics` | Update own biometrics details | [link]() |

### Biometrics - Weight
| `POST` | `api/me/biometrics/weights` | Add weight biometric | [link]() |
| `POST` | `api/me/biometrics/measures` | Add measure biometric | [link]() |
| `GET` | `api/me/biometrics/measures` | Add measure biometric | [link]() |

------------
### Biometrics
| HTTP Method | Endpoint | Description | Role | Details |
| --- | --- | --- | --- | --- |
| `GET` | `api/biometrics/{biometricId}` | Get the user biometrics | User | [link]() |
| `POST` | `api/bio` | Add a user | User | [link]() |
| `PUT` | `api/bio` | Update the user details | User | [link]() |
