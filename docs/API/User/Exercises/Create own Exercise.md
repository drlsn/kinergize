# Create own Exercise

Create your own exercise, e.g. if it's missing in a global listing.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; POST

### URL
&nbsp;&nbsp;&nbsp;&nbsp; /api/me/exercises

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
    "status": 400,
    "message": "string"
  }
}
```
