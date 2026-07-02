# V2 Customers My Invoices Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `invoice_items` | [`List[InvoiceItem]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/invoice-item.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.invoice_item import InvoiceItem
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.v_2_customers_my_invoices_response_1 import V2CustomersMyInvoicesResponse1

v_2_customers_my_invoices_response_1 = V2CustomersMyInvoicesResponse1(
    meta=Meta(
        total=6,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    invoice_items=[
        InvoiceItem(
            amount='12.34',
            description='a56e086a317d8410c8b4cfd1f4dc9f82',
            duration='744',
            duration_unit='Hours',
            end_time='2020-02-01T00:00:00Z',
            group_description='my-doks-cluster',
            product='Kubernetes Clusters',
            resource_uuid='711157cb-37c8-4817-b371-44fa3504a39c',
            start_time='2020-01-01T00:00:00Z',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        InvoiceItem(
            amount='34.45',
            description='Spaces ($5/mo 250GB storage & 1TB bandwidth)',
            duration='744',
            duration_unit='Hours',
            end_time='2020-02-01T00:00:00Z',
            product='Spaces Subscription',
            start_time='2020-01-01T00:00:00Z',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=3&per_page=2',
            next='https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=2&per_page=2',
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



