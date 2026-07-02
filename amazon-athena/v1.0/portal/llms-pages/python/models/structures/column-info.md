# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.

*This model accepts additional fields of type Any.*


# Class Name

`ColumnInfo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `str` | Optional | - |
| `schema_name` | `str` | Optional | - |
| `table_name` | `str` | Optional | - |
| `name` | `str` | Required | - |
| `label` | `str` | Optional | - |
| `mtype` | `str` | Required | - |
| `precision` | `int` | Optional | - |
| `scale` | `int` | Optional | - |
| `nullable` | [`ColumnNullable2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/column-nullable-2.md) | Optional | - |
| `case_sensitive` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.column_info import ColumnInfo

column_info = ColumnInfo(
    name='Name8',
    mtype='Type8',
    catalog_name='CatalogName2',
    schema_name='SchemaName8',
    table_name='TableName4',
    label='Label6',
    precision=110,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



