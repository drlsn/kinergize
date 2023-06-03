# Get Workouts Statistics
Get general statistics information about last of given amount of days of workouts.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; /api/me/statistics

*Example*
`/api/me/statistics?days=30`

### Headers Required
- Content-Type - application/json
- Authorization - "Bearer Token"

## Response

### Codes

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object of statistics

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- days - array of objects
  - object
    - date - string, parsable, e.g. 20.02.2023
    - weight - weight of the person doing exercise on this day
    - program - string, id or name of a program active at the time
    - session - string, the name of the session done on this day
    - muscles - array of objects
      - object
        - name - name of the muscle
        -  
    - exercises - array of objects ??
      - exercise-x 

#### 401
&nbsp;&nbsp;&nbsp;&nbsp; Missing, bad or expired access token.

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- error - string
  - status - integer
  - message - string

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```
{
  "error": {
    "status": 401,
    "message": "string"
  }
}
```
