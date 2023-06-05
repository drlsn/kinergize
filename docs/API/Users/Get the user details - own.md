# Get the user details - own

Get a specific user details.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/users/{userId}

### Minimum Role Required
User

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20Documentation.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Array of users and their names

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- array of objects
  - object
    - id - string
    - name - string
    - email - string
