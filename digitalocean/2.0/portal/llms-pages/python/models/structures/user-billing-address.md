# User Billing Address

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlVzZXJCaWxsaW5nQWRkcmVzcw

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`UserBillingAddress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address_line_1` | `str` | Optional | Street address line 1 |
| `address_line_2` | `str` | Optional | Street address line 2 |
| `city` | `str` | Optional | City |
| `country_iso_2_code` | `str` | Optional | Country (ISO2) code |
| `created_at` | `str` | Optional | Timestamp billing address was created |
| `postal_code` | `str` | Optional | Postal code |
| `region` | `str` | Optional | Region |
| `updated_at` | `str` | Optional | Timestamp billing address was updated |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.user_billing_address import UserBillingAddress

user_billing_address = UserBillingAddress(
    address_line_1='101 Shark Row',
    address_line_2='address_line26',
    city='Atlantis',
    country_iso_2_code='US',
    created_at='2019-09-03T16:34:46.000+00:00',
    postal_code='12345',
    region='OC',
    updated_at='2019-09-03T16:34:46.000+00:00',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



