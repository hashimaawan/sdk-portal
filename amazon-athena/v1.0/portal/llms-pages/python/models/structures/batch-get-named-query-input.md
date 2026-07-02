# Batch Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeUlucHV0

Contains an array of named query IDs.


# Class Name

`BatchGetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `named_query_ids` | `List[str]` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |


# Example

```python
from amazonathena.models.batch_get_named_query_input import BatchGetNamedQueryInput

batch_get_named_query_input = BatchGetNamedQueryInput(
    named_query_ids=[
        'NamedQueryIds3',
        'NamedQueryIds2',
        'NamedQueryIds1'
    ]
)
```



