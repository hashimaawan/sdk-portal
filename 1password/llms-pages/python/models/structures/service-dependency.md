# Service Dependency

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlNlcnZpY2VEZXBlbmRlbmN5

The state of a registered server dependency.

*This model accepts additional fields of type Any.*


# Class Name

`ServiceDependency`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | Human-readable message for explaining the current state. |
| `service` | `str` | Optional | - |
| `status` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.service_dependency import ServiceDependency

service_dependency = ServiceDependency(
    message='message0',
    service='service0',
    status='status2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



