# Get the user details - own

Get own user details.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/users/me

&nbsp;&nbsp;&nbsp;&nbsp; *Query Parameters*
- scope - string; optional; options: minimal, full; define how much detail data to receive

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

#### *Examples*  
```
api/users/me
{
  "id": "user-jnnfgj",
  "name": "John Smith",
  "email": "john.smith@gmail.com"
}
```
```
api/users/me?scope=min
{
  "id": "user-jnnfgj",
  "name": "John Smith",
  "email": "john.smith@gmail.com"
}
```
```
api/users/me?scope=full
{
  "id": "user-jnnfgj",
  "name": "John Smith",
  "email": "john.smith@gmail.com",
  "planAimId": "plan-aim-jfhspd"
}
```
