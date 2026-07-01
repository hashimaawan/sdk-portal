# Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkVycm9yMg

If issuance or renewal reports `failed`, this property contains information about what happened

*This model accepts additional fields of type Any.*


# Class Name

`Error2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `str` | Optional | - |
| `message` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.error_2 import Error2

error_2 = Error2(
    code='code8',
    message='message0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



