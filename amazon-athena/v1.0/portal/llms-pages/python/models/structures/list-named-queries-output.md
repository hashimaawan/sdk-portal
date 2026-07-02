# List Named Queries Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNPdXRwdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListNamedQueriesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_ids` | `List[str]` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_named_queries_output import ListNamedQueriesOutput

list_named_queries_output = ListNamedQueriesOutput(
    named_query_ids=[
        'NamedQueryIds9'
    ],
    next_token='NextToken0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



