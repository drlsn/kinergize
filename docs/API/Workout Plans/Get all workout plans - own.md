# Get all workout plans - own

Get list of all own workout plans.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/plans/me

### Minimum Role Required
User

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object containing an array of workout plans

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- object
  - values - array of objects
    - object
      - id - string
      - name - string

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```
{
  "values": [
    {
      "id": "plan-sdfbse",
      "name": "Push - Pull"
    },
    {
      "id": "plan-asdfaw"",
      "name": "Split"
    },
  ]
}
```
