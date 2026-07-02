# Delete Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRlbGV0ZU5hbWVkUXVlcnlJbnB1dA


# Class Name

`DeleteNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |


# Example

```python
from amazonathena.models.delete_named_query_input import DeleteNamedQueryInput

delete_named_query_input = DeleteNamedQueryInput(
    named_query_id='NamedQueryId6'
)
```



