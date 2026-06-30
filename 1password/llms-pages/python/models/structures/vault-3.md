# Vault 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlZhdWx0Mw

*This model accepts additional fields of type Any.*


# Class Name

`Vault3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.vault_3 import Vault3

vault_3 = Vault3(
    id='id8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



