# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database_list` | [`List[Database]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/database.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.database import Database
from amazonathena.models.list_databases_output import ListDatabasesOutput
from amazonathena.models.parameters import Parameters

list_databases_output = ListDatabasesOutput(
    database_list=[
        Database(
            name='Name4',
            description='Description8',
            parameters=Parameters(
                additional_properties={
                    'exampleAdditionalProperty': 'Parameters_additionalProperties2'
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    next_token='NextToken8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



