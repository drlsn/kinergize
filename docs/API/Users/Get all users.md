# Get all users

Get a list of all users, for administrators only.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/users

### Headers Required
- Content-Type - application/json
- Authorization - "Bearer Token"

## Response

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Array of users and their names

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- array of objects
  - object
    - id - string
    - name - string
    - email - string

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

#### 403
&nbsp;&nbsp;&nbsp;&nbsp; Authorization token is valid, but endpoint is forbidden for the role.

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
