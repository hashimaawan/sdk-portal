# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA


# Class Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `update_count` | `int` | Optional | - |
| `result_set` | [`ResultSet2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-set-2.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```python
from amazonathena.models.column_info import ColumnInfo
from amazonathena.models.datum import Datum
from amazonathena.models.get_query_results_output import GetQueryResultsOutput
from amazonathena.models.result_set_2 import ResultSet2
from amazonathena.models.result_set_metadata_2 import ResultSetMetadata2
from amazonathena.models.row import Row

get_query_results_output = GetQueryResultsOutput(
    update_count=242,
    result_set=ResultSet2(
        rows=[
            Row(
                data=[
                    Datum(
                        var_char_value='VarCharValue8'
                    ),
                    Datum(
                        var_char_value='VarCharValue8'
                    )
                ]
            ),
            Row(
                data=[
                    Datum(
                        var_char_value='VarCharValue8'
                    ),
                    Datum(
                        var_char_value='VarCharValue8'
                    )
                ]
            )
        ],
        result_set_metadata=ResultSetMetadata2(
            column_info=[
                ColumnInfo(
                    name='Name6',
                    mtype='Type6',
                    catalog_name='CatalogName0',
                    schema_name='SchemaName0',
                    table_name='TableName2',
                    label='Label4',
                    precision=48
                )
            ]
        )
    ),
    next_token='NextToken0'
)
```



