# Billing History

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkJpbGxpbmdIaXN0b3J5

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`BillingHistory`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `str` | Optional | Amount of the billing history entry. |
| `date` | `datetime` | Optional | Time the billing history entry occurred. |
| `description` | `str` | Optional | Description of the billing history entry. |
| `invoice_id` | `str` | Optional | ID of the invoice associated with the billing history entry, if  applicable. |
| `invoice_uuid` | `str` | Optional | UUID of the invoice associated with the billing history entry, if  applicable. |
| `mtype` | [`Type6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-6.md) | Optional | Type of billing history entry. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.billing_history import BillingHistory
from digitaloceanapi.models.type_6 import Type6

billing_history = BillingHistory(
    amount='12.34',
    date=dateutil.parser.parse('2018-06-01T08:44:38Z'),
    description='Invoice for May 2018',
    invoice_id='123',
    invoice_uuid='example-uuid',
    mtype=Type6.INVOICE,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



