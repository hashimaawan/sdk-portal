# List Application DPU Sizes Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzT3V0cHV0


# Class Name

`ListApplicationDPUSizesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `application_dpu_sizes` | [`List[ApplicationDPUSizes]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/application-dpu-sizes.md) | Optional | - |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```python
from amazonathena.models.application_dpu_sizes import ApplicationDPUSizes
from amazonathena.models.list_application_dpu_sizes_output import ListApplicationDPUSizesOutput

list_application_dpu_sizes_output = ListApplicationDPUSizesOutput(
    application_dpu_sizes=[
        ApplicationDPUSizes(
            application_runtime_id='ApplicationRuntimeId0',
            supported_dpu_sizes=[
                113,
                114
            ]
        )
    ],
    next_token='NextToken6'
)
```



