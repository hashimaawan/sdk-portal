# Row

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJvdw

The rows that make up a query result table.


# Class Name

`Row`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[Datum]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/datum.md) | Optional | - |


# Example

```python
from amazonathena.models.datum import Datum
from amazonathena.models.row import Row

row = Row(
    data=[
        Datum(
            var_char_value='VarCharValue8'
        )
    ]
)
```



