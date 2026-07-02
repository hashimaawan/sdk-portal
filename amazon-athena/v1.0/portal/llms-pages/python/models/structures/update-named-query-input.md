# Update Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Any.*


# Class Name

`UpdateNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `name` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `query_string` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.update_named_query_input import UpdateNamedQueryInput

update_named_query_input = UpdateNamedQueryInput(
    named_query_id='NamedQueryId8',
    name='Name4',
    query_string='QueryString6',
    description='Description2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



