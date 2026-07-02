# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | [`Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/database-2.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.database_2 import Database2
from amazonathena.models.get_database_output import GetDatabaseOutput
from amazonathena.models.parameters import Parameters

get_database_output = GetDatabaseOutput(
    database=Database2(
        name='Name2',
        description='Description8',
        parameters=Parameters(
            additional_properties={
                'exampleAdditionalProperty': 'Parameters_additionalProperties2'
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



