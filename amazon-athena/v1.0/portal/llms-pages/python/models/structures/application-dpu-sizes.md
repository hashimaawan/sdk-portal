# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.


# Class Name

`ApplicationDPUSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `application_runtime_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `supported_dpu_sizes` | `List[int]` | Optional | - |


# Example

```python
from amazonathena.models.application_dpu_sizes import ApplicationDPUSizes

application_dpu_sizes = ApplicationDPUSizes(
    application_runtime_id='ApplicationRuntimeId8',
    supported_dpu_sizes=[
        137
    ]
)
```



