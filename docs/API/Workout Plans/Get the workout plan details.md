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
&nbsp;&nbsp;&nbsp;&nbsp; Object with workout plan details

#### *Fields*
- object
  - identity - object
    - id - string
    - name - string
  - author - object
    - id - string
    - name - string
  - sessions - array of objects
    - object
      - id - id of a session
      - type - type of a session; active, rest
      - name - name of a session

#### *Examples*  
```
api/plans/{planId}
{
  "identity": {
    "id": "plan-jnnfgj",
    "name": "Push - Pull",
  },
  "author": {
    "id": "user-jnnfgj",
    "name": "John Smith",
  },
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
