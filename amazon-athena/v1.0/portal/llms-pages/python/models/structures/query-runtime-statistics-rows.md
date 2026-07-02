# Query Runtime Statistics Rows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NSb3dz

Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query.

*This model accepts additional fields of type Any.*


# Class Name

`QueryRuntimeStatisticsRows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `input_rows` | `int` | Optional | - |
| `input_bytes` | `int` | Optional | - |
| `output_bytes` | `int` | Optional | - |
| `output_rows` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.query_runtime_statistics_rows import QueryRuntimeStatisticsRows

query_runtime_statistics_rows = QueryRuntimeStatisticsRows(
    input_rows=100,
    input_bytes=136,
    output_bytes=94,
    output_rows=104,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



