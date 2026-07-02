# Service Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNlcnZpY2UlMjUyMGNvbXBvbmVudHMlMjUyMHRoYXQlMjUyMGFyZSUyNTIwcGFydCUyNTIwb2YlMjUyMHRoaXMlMjUyMGRlcGxveW1lbnQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ServiceComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | - |
| `source_commit_hash` | `str` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.service_components_that_are_part_of_this_deployment import ServiceComponentsThatArePartOfThisDeployment

service_components_that_are_part_of_this_deployment = ServiceComponentsThatArePartOfThisDeployment(
    name='web',
    source_commit_hash='54d4a727f457231062439895000d45437c7bb405',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



