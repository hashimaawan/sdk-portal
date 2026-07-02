# Row

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJvdw

The rows that make up a query result table.

*This model accepts additional fields of type Any.*


# Class Name

`Row`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[Datum]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/datum.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.datum import Datum
from amazonathena.models.row import Row

row = Row(
    data=[
        Datum(
            var_char_value='VarCharValue8',
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



