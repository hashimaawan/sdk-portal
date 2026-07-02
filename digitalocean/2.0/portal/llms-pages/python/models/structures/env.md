# Env

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkVudg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Env`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `str` | Required | The variable name<br><br>**Constraints**: *Pattern*: `^[_A-Za-z][_A-Za-z0-9]*$` |
| `scope` | [`Scope`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/scope.md) | Optional | - RUN_TIME: Made available only at run-time<br>- BUILD_TIME: Made available only at build-time<br>- RUN_AND_BUILD_TIME: Made available at both build and run-time<br><br>**Default**: `"RUN_AND_BUILD_TIME"` |
| `mtype` | [`Type2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-2.md) | Optional | - GENERAL: A plain-text environment variable<br>- SECRET: A secret encrypted environment variable<br><br>**Default**: `"GENERAL"` |
| `value` | `str` | Optional | The value. If the type is `SECRET`, the value will be encrypted on first submission. On following submissions, the encrypted value should be used. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.env import Env
from digitaloceanapi.models.scope import Scope
from digitaloceanapi.models.type_2 import Type2

env = Env(
    key='BASE_URL',
    scope=Scope.BUILD_TIME,
    mtype=Type2.GENERAL,
    value='http://example.com',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



