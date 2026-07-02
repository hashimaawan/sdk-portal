# List Query Executions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListQueryExecutionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_ids` | `List[str]` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_query_executions_output import ListQueryExecutionsOutput

list_query_executions_output = ListQueryExecutionsOutput(
    query_execution_ids=[
        'QueryExecutionIds3',
        'QueryExecutionIds4'
    ],
    next_token='NextToken6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



