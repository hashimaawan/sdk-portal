# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkZpcmV3YWxsNA

*This model accepts additional fields of type Any.*


# Class Name

`Firewall4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewall` | `int` | Optional | ID of the Firewall |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.firewall_4 import Firewall4

firewall_4 = Firewall4(
    firewall=108,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



