# Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkVuZHBvaW50

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Endpoint`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate_id` | `uuid\|str` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `created_at` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the CDN endpoint was created. |
| `custom_domain` | `str` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `endpoint` | `str` | Optional, Read-only | The fully qualified domain name (FQDN) from which the CDN-backed content is served. |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference a CDN endpoint. |
| `origin` | `str` | Required | The fully qualified domain name (FQDN) for the origin server which provides the content for the CDN. This is currently restricted to a Space. |
| `ttl` | [`Ttl`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `3600` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.endpoint import Endpoint
from digitaloceanapi.models.ttl import Ttl

endpoint = Endpoint(
    origin='static-images.nyc3.digitaloceanspaces.com',
    certificate_id='892071a0-bb95-49bc-8021-3afd67a210bf',
    created_at=dateutil.parser.parse('2018-03-21T16:02:37Z'),
    custom_domain='static.example.com',
    endpoint='static-images.nyc3.cdn.digitaloceanspaces.com',
    id='892071a0-bb95-49bc-8021-3afd67a210bf',
    ttl=Ttl.ENUM_3600,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



