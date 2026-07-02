# Database 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFiYXNlMg

*This model accepts additional fields of type Any.*


# Class Name

`Database2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/parameters.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.database_2 import Database2
from amazonathena.models.parameters import Parameters

database_2 = Database2(
    name='Name2',
    description='Description4',
    parameters=Parameters(
        additional_properties={
            'exampleAdditionalProperty': 'Parameters_additionalProperties2'
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



