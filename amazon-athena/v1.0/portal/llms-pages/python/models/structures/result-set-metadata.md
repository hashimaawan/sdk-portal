# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.

*This model accepts additional fields of type Any.*


# Class Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `column_info` | [`List[ColumnInfo]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/column-info.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.column_info import ColumnInfo
from amazonathena.models.result_set_metadata import ResultSetMetadata

result_set_metadata = ResultSetMetadata(
    column_info=[
        ColumnInfo(
            name='Name6',
            mtype='Type6',
            catalog_name='CatalogName0',
            schema_name='SchemaName0',
            table_name='TableName2',
            label='Label4',
            precision=48,
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



