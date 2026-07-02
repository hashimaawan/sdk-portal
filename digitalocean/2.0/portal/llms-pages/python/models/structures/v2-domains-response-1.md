# V2 Domains Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DomainsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domain` | [`Domain1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/domain-1.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.domain_1 import Domain1
from digitaloceanapi.models.v_2_domains_response_1 import V2DomainsResponse1

v_2_domains_response_1 = V2DomainsResponse1(
    domain=Domain1(
        ip_address='ip_address6',
        name='example.com',
        ttl=1800,
        zone_file=None,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



