# Create own Exercise

Create your own exercise, e.g. if it's missing in a global listing.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; POST

### URL
&nbsp;&nbsp;&nbsp;&nbsp; /api/me/exercises

### Headers Required
- Content-Type - application/json
- Authorization - "Bearer Token"

### Body
- name - string, required, a name of the exercise to create
- muscle - string, required, a name of a muscle the exercise is targeting; to choose from limited set of options (chest, back, legs, shoulders, biceps, triceps, abs)

*Example*
```
{
  "name": "Dumbbell Press",
  "muscle": "chest"
}
```

## Response

### Codes

#### 201
&nbsp;&nbsp;&nbsp;&nbsp; The exercise has been successfully added to the users exercise list.

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
