# Functions Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkZ1bmN0aW9ucyUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`FunctionsComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | - |
| `namespace` | `str` | Optional | The namespace where the functions are deployed. |
| `source_commit_hash` | `str` | Optional | The commit hash of the repository that was used to build this functions component. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.functions_components_that_are_part_of_this_deployment import FunctionsComponentsThatArePartOfThisDeployment

functions_components_that_are_part_of_this_deployment = FunctionsComponentsThatArePartOfThisDeployment(
    name='my-functions-component',
    namespace='ap-b2a93513-8d9b-4223-9d61-5e7272c81c32',
    source_commit_hash='54d4a727f457231062439895000d45437c7bb405',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



