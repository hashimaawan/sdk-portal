# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`ListApplicationDpuSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `application_dpu_sizes` | [`List[ApplicationDpuSizes]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/application-dpu-sizes.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.application_dpu_sizes import ApplicationDpuSizes
from amazonathena.models.list_application_dpu_sizes_output import ListApplicationDpuSizesOutput

list_application_dpu_sizes_output = ListApplicationDpuSizesOutput(
    application_dpu_sizes=[
        ApplicationDpuSizes(
            application_runtime_id='ApplicationRuntimeId0',
            supported_dpu_sizes=[
                113,
                114
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    next_token='NextToken6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



