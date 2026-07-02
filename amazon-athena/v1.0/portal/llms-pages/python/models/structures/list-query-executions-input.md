# List Query Executions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`ListQueryExecutionsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `int` | Optional | **Constraints**: `>= 0`, `<= 50` |
| `work_group` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_query_executions_input import ListQueryExecutionsInput

list_query_executions_input = ListQueryExecutionsInput(
    next_token='NextToken0',
    max_results=50,
    work_group='WorkGroup2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



