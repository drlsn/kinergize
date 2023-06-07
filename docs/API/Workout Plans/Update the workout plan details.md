# Update the workout plan details

Update the workout plan details.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; PUT

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/plans/{planId}

### Minimum Role Required
&nbsp;&nbsp;&nbsp;&nbsp; User

### Body
&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- object
  - id - string
  - name - string
  - sessionsPerDay - int - count of preferred sessions to be performed per day
  - sessions - array of objects
    - object
      - id - id of a session; if specified then type = active
      - type - type of a session; if specified as rest then other not required

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```
{
  "id": "plan-jnnfgj",
  "name": "Push - Pull",
  "sessionsPerDay": 1,
  "sessions": [
    {
      "id": "session-jfdimn",
    },
    {
      "id": "session-asdfwf",
    },
    {
      "type": "rest",
    },
    {
      "id": "session-jfdimn",
    },
    {
      "id": "session-asdfwf",
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

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; No body
