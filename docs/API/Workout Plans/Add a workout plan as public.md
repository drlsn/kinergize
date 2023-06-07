# Add a workout plan as public

Add your a workout plan as public, for administartors only.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; POST

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/plans/public

### Minimum Role Required
&nbsp;&nbsp;&nbsp;&nbsp; Admin

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
