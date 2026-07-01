# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM

*This model accepts additional fields of type Any.*


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `values` | List[List[float \| str]] | Required | This is 2d List of a container for one-of cases. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.time_series import TimeSeries

time_series = TimeSeries(
    values=[
        [
            161.02,
            161.03
        ],
        [
            161.02,
            161.03
        ]
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



