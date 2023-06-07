# Kinergize - API General Info

## API calls
The Kinergize API is a Web API with different endpoints which return JSON metadata about workout plans, workout session and statistics.

## Base URL
The base address of Web API is https://kinergize.me/api.

## Requests
Data resources are accessed via standard HTTP requests in UTF-8 format to an API endpoint. The Web API uses the following HTTP verbs:
| Http Method | Description |
| --- | --- |
| GET | Retrieves resources |
| POST | Creates resources |
| PUT | Changes and/or replaces resources or collections |
| DELETE | Deletes resources |

## Responses
Web API normally returns JSON in the response body. Some endpoints don't return JSON but the HTTP status code.

### Response Error
| Key | Value Type | Value Description |
| --- | --- | --- |
| status | integer | The HTTP status code |
| message | string | A short description of the cause of the error. |

*Example:*
```
HTTP/1.1 400 Bad Request
{
    "error": 
    {
        "status": 400,
        "message": "invalid id"
    }
}
```

## Pagination

Some endpoints support a way of paging the dataset, taking an offset and limit as query parameters:
https://kinergize.me/api/exercises?discipline=calisthenics&limit=100&offset=20
