# Add a workout plan - own, private

Add your own workout plan.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; POST

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/plans/me

### Minimum Role Required
&nbsp;&nbsp;&nbsp;&nbsp; User

### Body

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- object
  - name - string; name of the created workout plan

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```
{
  "name": "Push - Pull"
}
```

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 201
&nbsp;&nbsp;&nbsp;&nbsp; No body
