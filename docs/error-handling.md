# Error Handling

HTTP status codes provide the request results; a successful response will return a 2## status code while an error will return a 4## or 5## status code.

| Code   | Description   | Details                                                                                                         |
| -------|-------------- | --------------------------------------------------------------------------------------------------------------- | 
| 200    | OK            | Request was successful and the response contains data.                                                          |
| 201    | Created       | Request was successful and a resource was created. The response does not contain data.                          |
| 204    | No Content    | Request was successful. The response does not contain data.                                                     |
| 400    | Bad Request   | Invalid and or missing data.                                                                                    |
| 401    | Unauthorized  | Invalid credentials or the user does not have access to the data.                                               |
| 404    | Not Found     | Endpoint is invalid or does not exist.                                                                          |
| 500    | Server Error  | The request unexpectedly failed. If a request continues to fail with a 500 status code, please contact [Client Care](https://help.avanti.ca/support/tickets/new). |

## Error Responses


Error responses are sent as a [RFC 7807 - Problem Details](https://tools.ietf.org/html/rfc7807) compliant payload. Typically, error messages are returned as short descriptive error codes such as **required** or **invalid_characters**. When an error contains context-specific information,  a full error message will be returned instead.

Field names are not case sensitive and can be sent as pascal case or camel case. Fields can contain more than one error. If the error is not field-specific, it will be returned without a field name.

##### Error response with invalid fields

```
{
    "title": "One or more validation errors occurred.",
    "status": 400,
    "errors": {
        "": [
            "max_entries_exceeded"
        ],
        "Name": [
            "invalid_max_length",
            "invalid_characters"
        ],
        "Email": [
            "invalid_email"
        ]
    }
}
```

##### Unauthorized error response

```
{
    "title": "Unauthorized",
    "status": 401
}
```
