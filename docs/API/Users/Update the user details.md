# Update the user details

Update own user details like name.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; PUT

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/users/me

### Minimum Role Required
&nbsp;&nbsp;&nbsp;&nbsp; User

### Body
&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- object
  - name - string

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```
{
  "name": "John Watson",
}
```

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; No body
