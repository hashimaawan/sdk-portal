# Vault 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlZhdWx0MQ

*This model accepts additional fields of type Any.*


# Class Name

`Vault1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Required | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from m1passwordconnect.models.vault_1 import Vault1

vault_1 = Vault1(
    id='id0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



