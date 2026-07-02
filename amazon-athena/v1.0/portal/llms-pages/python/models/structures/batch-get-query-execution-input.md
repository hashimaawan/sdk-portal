# Batch Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25JbnB1dA

Contains an array of query execution IDs.

*This model accepts additional fields of type Any.*


# Class Name

`BatchGetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `query_execution_ids` | `List[str]` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.batch_get_query_execution_input import BatchGetQueryExecutionInput

batch_get_query_execution_input = BatchGetQueryExecutionInput(
    query_execution_ids=[
        'QueryExecutionIds7'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



