# Vault

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0bSUyRlZhdWx0

*This model accepts additional fields of type Any.*


# Class Name

`Vault`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attribute_version` | `int` | Optional | The vault version |
| `content_version` | `int` | Optional | The version of the vault contents |
| `created_at` | `datetime` | Optional, Read-only | - |
| `description` | `str` | Optional | - |
| `id` | `str` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `items` | `int` | Optional | Number of active items in the vault |
| `name` | `str` | Optional | - |
| `mtype` | [`Type2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/enumerations/type-2.md) | Optional | - |
| `updated_at` | `datetime` | Optional, Read-only | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from m1passwordconnect.models.vault import Vault

vault = Vault(
    attribute_version=108,
    content_version=228,
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    description='description6',
    id='id6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



