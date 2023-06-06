# Get the exercise details

Get a specific exercise description details.

## Request

### HTTP Method
&nbsp;&nbsp;&nbsp;&nbsp; GET

### URL
&nbsp;&nbsp;&nbsp;&nbsp; api/exercises/{exerciseId}

### Minimum Role Required
User

## Success Response

&nbsp;&nbsp;&nbsp;&nbsp; [*More Info*](../Kinergize%20-%20API%20General%20Info.md)

#### 200
&nbsp;&nbsp;&nbsp;&nbsp; Object of exercise details

&nbsp;&nbsp;&nbsp;&nbsp; *Fields*
- object
  - pageTitle - string
  - name - string
  - description - string
  - properties - array of objects
    - object
      - type - string; type of the exercise property
      - name - string; localized name of the exercise property
      - selectedOptionId - string; id of selected option
      - options - array of objects
        - id - string; id of a property value to be selected
        - name - string; localized name of the property value

&nbsp;&nbsp;&nbsp;&nbsp; *Example*
```                                           
{          
  "pageTitle": "Exercise Details",
  "name": "Lying Chest Dumbbell Press",
  "description": "...",
  "properties": [
    {
	  "type": "author",
	  "name": "Author",
	  "valueId": "public",
	  "values": [
		{
		  "id": "public",
		  "name": "Public"
		},
		{
		  "id": "public",
		  "name": "Own"
		},
		{
		  "id": "any",
		  "name": "Any"
		}
	  ]
	},
	{
	  "type": "discipline",
	  "name": "Discipline",
	  "valueId": "weight-lifting",
	  "values": [
		{
		  "id": "weight-lifting",
		  "name": "Weight Lifting"
		},
		{
		  "id": "calisthenics",
		  "name": "Calisthenics"
		},
		{
		  "id": "any",
		  "name": "Any"
		}
	  ]
    }
  ]
}

```
