# Get all users

Get a list of all users, for administrators only.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/users

### Minimum Role Required
Admin

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object containing an array of users

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
      "id": "user-sdfbse",
      "name": "Douglas"
    },
    {
      "id": "user-asdfaw"",
      "name": "Sean"
    },
  ]
}
```
