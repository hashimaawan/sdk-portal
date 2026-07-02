# List Engine Versions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc0lucHV0


# Class Name

`ListEngineVersionsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 10` |


# Example

```python
from amazonathena.models.list_engine_versions_input import ListEngineVersionsInput

list_engine_versions_input = ListEngineVersionsInput(
    next_token='NextToken0',
    max_results=10
)
```



