# Health Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRkhlYWx0aCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`HealthResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dependencies` | [`List[ServiceDependency]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/service-dependency.md) | Optional | - |
| `name` | `str` | Required | - |
| `version` | `str` | Required | The Connect server's version |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.health_response import HealthResponse
from m1passwordconnect.models.service_dependency import ServiceDependency

health_response = HealthResponse(
    name='name6',
    version='version2',
    dependencies=[
        ServiceDependency(
            message='message6',
            service='service6',
            status='status8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ServiceDependency(
            message='message6',
            service='service6',
            status='status8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



