# Get the user details - own

Get own user details.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/users/me

### Minimum Role Required
User

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Array of user ids

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
  "email": "john.smith@gmail.com"
}
```
