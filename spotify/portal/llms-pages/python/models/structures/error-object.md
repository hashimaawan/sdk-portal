# Error Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRkVycm9yT2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`ErrorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | `int` | Required | The HTTP status code (also returned in the response header; see [Response Status Codes](/documentation/web-api/concepts/api-calls#response-status-codes) for more information).<br><br>**Constraints**: `>= 400`, `<= 599` |
| `message` | `str` | Required | A short description of the cause of the error. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.error_object import ErrorObject

error_object = ErrorObject(
    status=400,
    message='message0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



