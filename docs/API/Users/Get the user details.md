# Get the user details

Get a specific user details.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/users/{userId}

### Minimum Role Required
Admin

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object of user details

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- array of objects
  - object
    - id - string
    - name - string
    - email - string

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```
{
  "id": "user-jnnfgj",
  "name": "John Smith",
  "email": "john.smith@gmail.com",
}
```
