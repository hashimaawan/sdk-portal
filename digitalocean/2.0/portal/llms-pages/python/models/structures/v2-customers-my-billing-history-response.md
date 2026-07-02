# V2 Customers My Billing History Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCaWxsaW5nJTI1MjBIaXN0b3J5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2CustomersMyBillingHistoryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billing_history` | [`List[BillingHistory]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/billing-history.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta-1.md) | Required | Information about the response itself. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.billing_history import BillingHistory
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta_1 import Meta1
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.type_6 import Type6
from digitaloceanapi.models.v_2_customers_my_billing_history_response import V2CustomersMyBillingHistoryResponse

v_2_customers_my_billing_history_response = V2CustomersMyBillingHistoryResponse(
    meta=Meta1(
        total=5,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    billing_history=[
        BillingHistory(
            amount='12.34',
            date=dateutil.parser.parse('2018-06-01T08:44:38Z'),
            description='Invoice for May 2018',
            invoice_id='123',
            invoice_uuid='example-uuid',
            mtype=Type6.INVOICE,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        BillingHistory(
            amount='-12.34',
            date=dateutil.parser.parse('2018-06-02T08:44:38Z'),
            description='Payment (MC 2018)',
            invoice_id='invoice_id6',
            invoice_uuid='invoice_uuid4',
            mtype=Type6.PAYMENT,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='https://api.digitalocean.com/v2/customers/my/billing_history?page=3&per_page=2',
            next='https://api.digitalocean.com/v2/customers/my/billing_history?page=2&per_page=2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



