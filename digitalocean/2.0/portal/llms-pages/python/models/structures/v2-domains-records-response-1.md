# V2 Domains Records Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DomainsRecordsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domain_record` | [`DomainRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/domain-record.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.domain_record import DomainRecord
from digitaloceanapi.models.v_2_domains_records_response_1 import V2DomainsRecordsResponse1

v_2_domains_records_response_1 = V2DomainsRecordsResponse1(
    domain_record=DomainRecord(
        mtype='A',
        data='162.10.66.0',
        flags=None,
        id=28448433,
        name='www',
        port=None,
        priority=None,
        tag=None,
        ttl=1800,
        weight=None,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



