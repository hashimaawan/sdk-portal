# V2 Domains Records Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DomainsRecordsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `domain_records` | [`List[DomainRecord]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/domain-record.md) | Optional | - |
| `links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/meta.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.domain_record import DomainRecord
from digitaloceanapi.models.links import Links
from digitaloceanapi.models.meta import Meta
from digitaloceanapi.models.pages import Pages
from digitaloceanapi.models.v_2_domains_records_response import V2DomainsRecordsResponse

v_2_domains_records_response = V2DomainsRecordsResponse(
    meta=Meta(
        total=1,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    domain_records=[
        DomainRecord(
            mtype='type8',
            data='data2',
            flags=216,
            id=172,
            name='name2',
            port=92,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        DomainRecord(
            mtype='type8',
            data='data2',
            flags=216,
            id=172,
            name='name2',
            port=92,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        DomainRecord(
            mtype='type8',
            data='data2',
            flags=216,
            id=172,
            name='name2',
            port=92,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    links=Links(
        pages=Pages(
            last='last6',
            next='next2',
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



