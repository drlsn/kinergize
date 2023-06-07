# Get all workout plans - public.md

Get a list of all public workout plans.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/plans/public

### Minimum Role Required
Guest

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object containing an array of workout plan ids

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- object
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
