# Product Charges

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlByb2R1Y3RDaGFyZ2Vz

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`ProductCharges`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `str` | Optional | Total amount charged |
| `items` | [`List[Item]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/item.md) | Optional | List of amount, and grouped aggregates by resource type. |
| `name` | `str` | Optional | Description of usage charges |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.item import Item
from digitaloceanapi.models.product_charges import ProductCharges

product_charges = ProductCharges(
    amount='12.34',
    items=[
        Item(
            amount='10.00',
            count='1',
            name='Spaces Subscription',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Item(
            amount='2.34',
            count='1',
            name='Database Clusters',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    name='Product usage charges',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



