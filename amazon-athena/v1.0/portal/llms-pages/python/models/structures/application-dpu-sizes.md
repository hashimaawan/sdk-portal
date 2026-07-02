# Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkFwcGxpY2F0aW9uRFBVU2l6ZXM

Contains the application runtime IDs and their supported DPU sizes.

*This model accepts additional fields of type Any.*


# Class Name

`ApplicationDpuSizes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `application_runtime_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `supported_dpu_sizes` | `List[int]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.application_dpu_sizes import ApplicationDpuSizes

application_dpu_sizes = ApplicationDpuSizes(
    application_runtime_id='ApplicationRuntimeId8',
    supported_dpu_sizes=[
        137
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



