# Invoice Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkludm9pY2VJdGVt

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`InvoiceItem`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `str` | Optional | Billed amount of this invoice item. Billed in USD. |
| `description` | `str` | Optional | Description of the invoice item. |
| `duration` | `str` | Optional | Duration of time this invoice item was used and subsequently billed. |
| `duration_unit` | `str` | Optional | Unit of time for duration. |
| `end_time` | `str` | Optional | Time the invoice item stopped being billed for usage. |
| `group_description` | `str` | Optional | Description of the invoice item when it is a grouped set of usage, such  as DOKS or databases. |
| `product` | `str` | Optional | Name of the product being billed in the invoice item. |
| `project_name` | `str` | Optional | Name of the DigitalOcean Project this resource belongs to. |
| `resource_id` | `str` | Optional | ID of the resource billing in the invoice item if available. |
| `resource_uuid` | `str` | Optional | UUID of the resource billing in the invoice item if available. |
| `start_time` | `str` | Optional | Time the invoice item began to be billed for usage. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.invoice_item import InvoiceItem

invoice_item = InvoiceItem(
    amount='12.34',
    description='a56e086a317d8410c8b4cfd1f4dc9f82',
    duration='744',
    duration_unit='Hours',
    end_time='2020-02-01T00:00:00Z',
    group_description='my-doks-cluster',
    product='Kubernetes Clusters',
    project_name='web',
    resource_id='2353624',
    resource_uuid='711157cb-37c8-4817-b371-44fa3504a39c',
    start_time='2020-01-01T00:00:00Z',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



