# Get all workout plans

Get a list of all workout plans, for administrators only.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/plans

### Minimum Role Required
Admin

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object containing an array of workout plan ids

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- array of strings

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```
{
  [
    "plan-sdfbse",
    "plan-jnnfgj",  
    "plan-asdfaw",  
    "plan-ewseft",  
    "plan-asdvew"  
  ]
}
```
