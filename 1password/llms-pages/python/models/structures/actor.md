# Actor

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkFjdG9y

*This model accepts additional fields of type Any.*


# Class Name

`Actor`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account` | `str` | Optional | - |
| `id` | `uuid\|str` | Optional | - |
| `jti` | `str` | Optional | - |
| `request_ip` | `str` | Optional | - |
| `user_agent` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.actor import Actor

actor = Actor(
    account='account0',
    id='0000193c-0000-0000-0000-000000000000',
    jti='jti2',
    request_ip='requestIp4',
    user_agent='userAgent6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



