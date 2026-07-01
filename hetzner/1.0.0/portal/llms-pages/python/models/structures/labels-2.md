# Labels 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxhYmVsczI

User-defined labels (key-value pairs)

*This model accepts additional fields of type Any.*


# Class Name

`Labels2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelkey` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.labels_2 import Labels2

labels_2 = Labels2(
    labelkey='value',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



