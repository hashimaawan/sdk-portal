# Labels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxhYmVscw

User-defined labels (key-value pairs)

*This model accepts additional fields of type Any.*


# Class Name

`Labels`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelkey` | `str` | Optional | New label |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.labels import Labels

labels = Labels(
    labelkey='value',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



