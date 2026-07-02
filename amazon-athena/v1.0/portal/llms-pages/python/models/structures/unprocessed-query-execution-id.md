# Unprocessed Query Execution Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUXVlcnlFeGVjdXRpb25JZA

Describes a query execution that failed to process.

*This model accepts additional fields of type Any.*


# Class Name

`UnprocessedQueryExecutionId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `error_code` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `error_message` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.unprocessed_query_execution_id import UnprocessedQueryExecutionId

unprocessed_query_execution_id = UnprocessedQueryExecutionId(
    query_execution_id='QueryExecutionId8',
    error_code='ErrorCode4',
    error_message='ErrorMessage6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



