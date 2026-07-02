# Sticky Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlN0aWNreVNlc3Npb25z

An object specifying sticky sessions settings for the load balancer.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`StickySessions`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cookie_name` | `str` | Optional | The name of the cookie sent to the client. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `cookie_ttl_seconds` | `int` | Optional | The number of seconds until the cookie set by the load balancer expires. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `mtype` | [`Type16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-16.md) | Optional | An attribute indicating how and if requests from a client will be persistently served by the same backend Droplet. The possible values are `cookies` or `none`.<br><br>**Default**: `"none"` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.sticky_sessions import StickySessions
from digitaloceanapi.models.type_16 import Type16

sticky_sessions = StickySessions(
    cookie_name='DO-LB',
    cookie_ttl_seconds=300,
    mtype=Type16.COOKIES,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



