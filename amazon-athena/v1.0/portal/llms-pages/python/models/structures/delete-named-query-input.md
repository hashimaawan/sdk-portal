# Delete Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRlbGV0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`DeleteNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.delete_named_query_input import DeleteNamedQueryInput

delete_named_query_input = DeleteNamedQueryInput(
    named_query_id='NamedQueryId6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



