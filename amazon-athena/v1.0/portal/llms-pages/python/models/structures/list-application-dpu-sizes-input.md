# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ

*This model accepts additional fields of type Any.*


# Class Name

`ListApplicationDpuSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.list_application_dpu_sizes_input import ListApplicationDpuSizesInput

list_application_dpu_sizes_input = ListApplicationDpuSizesInput(
    max_results=76,
    next_token='NextToken6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



