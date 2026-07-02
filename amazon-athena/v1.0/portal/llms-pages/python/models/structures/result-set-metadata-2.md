# Result Set Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRhMg


# Class Name

`ResultSetMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `column_info` | [`List[ColumnInfo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/column-info.md) | Optional | - |


# Example

```python
from amazonathena.models.column_info import ColumnInfo
from amazonathena.models.result_set_metadata_2 import ResultSetMetadata2

result_set_metadata_2 = ResultSetMetadata2(
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
```



