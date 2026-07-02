# List of TXT Validation Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3QlMjUyMG9mJTI1MjBUWFQlMjUyMHZhbGlkYXRpb24lMjUyMHJlY29yZA

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ListOfTxtValidationRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `txt_name` | `str` | Optional, Read-only | - |
| `txt_value` | `str` | Optional, Read-only | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.list_of_txt_validation_record import ListOfTxtValidationRecord

list_of_txt_validation_record = ListOfTxtValidationRecord(
    txt_name='_acme-challenge.app.example.com',
    txt_value='lXLOcN6cPv0nproViNcUHcahD9TrIPlNgdwesj0pYpk',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



