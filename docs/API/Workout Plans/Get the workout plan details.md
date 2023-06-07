# Get the workout plan details

Get details of the workout plan.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/plans/{planId}

&nbsp;&nbsp;&nbsp;&nbsp; *Query Parameters*
- scope - string; optional; options: min (default), full; define how much detail data to receive

### Minimum Role Required
User

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object with user details

#### *Fields*
- array of objects
  - object
    - id - string
    - name - string
    - email - string
    - planAimId - string - id of current workout plan
    - sessions - array of objects
      - object
        - id - id of a session
        - type - type of a session; active, rest
        - name - name of a session

#### *Examples*  
```
api/plans/{planId}
{
  "id": "plan-jnnfgj",
  "name": "Push - Pull",
  "sessionsPerDay": 1,
  "sessions": [
    {
      "id": "session-jfdimn",
      "type": "active",
      "name": "Push-Pull Session 1 - Chest, Shoulders, Triceps, Legs"
    },
    {
      "id": "session-asdfwf",
      "type": "active",
      "name": "Push-Pull Session 2 - Back, Biceps, Abs"
    },
    {
      "type": "rest",
    },
    {
      "id": "session-jfdimn",
      "type": "active",
      "name": "Push-Pull Session 1 - Chest, Shoulders, Triceps, Legs"
    },
    {
      "id": "session-asdfwf",
      "type": "active",
      "name": "Push-Pull Session 2 - Back, Biceps, Abs"
    },
    {
      "type": "rest",
    },
    {
      "type": "rest",
    },
  ]
}
```
