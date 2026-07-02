# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ


# Class Name

`ListApplicationDPUSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```python
from amazonathena.models.list_application_dpu_sizes_input import ListApplicationDPUSizesInput

list_application_dpu_sizes_input = ListApplicationDPUSizesInput(
    max_results=76,
    next_token='NextToken6'
)
```



