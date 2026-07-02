# Get Query Runtime Statistics Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`GetQueryRuntimeStatisticsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_query_runtime_statistics_input import GetQueryRuntimeStatisticsInput

get_query_runtime_statistics_input = GetQueryRuntimeStatisticsInput(
    query_execution_id='QueryExecutionId0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



