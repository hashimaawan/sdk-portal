# Stop Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0b3BRdWVyeUV4ZWN1dGlvbklucHV0

*This model accepts additional fields of type Any.*


# Class Name

`StopQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.stop_query_execution_input import StopQueryExecutionInput

stop_query_execution_input = StopQueryExecutionInput(
    query_execution_id='QueryExecutionId6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



