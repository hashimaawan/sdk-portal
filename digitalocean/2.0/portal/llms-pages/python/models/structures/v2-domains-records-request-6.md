# V2 Domains Records Request 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXF1ZXN0Ng

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DomainsRecordsRequest6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `str` | Optional | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `flags` | `int` | Optional | An unsigned integer between 0-255 used for CAA records. |
| `id` | `int` | Optional, Read-only | A unique identifier for each domain record. |
| `name` | `str` | Optional | The host name, alias, or service being defined by the record. |
| `port` | `int` | Optional | The port for SRV records. |
| `priority` | `int` | Optional | The priority for SRV and MX records. |
| `tag` | `str` | Optional | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `ttl` | `int` | Required | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `mtype` | `str` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `weight` | `int` | Optional | The weight for SRV records. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_domains_records_request_6 import V2DomainsRecordsRequest6

v_2_domains_records_request_6 = V2DomainsRecordsRequest6(
    ttl=1800,
    mtype='NS',
    data='ns1.digitalocean.com',
    flags=120,
    id=28448429,
    name='@',
    port=252,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



