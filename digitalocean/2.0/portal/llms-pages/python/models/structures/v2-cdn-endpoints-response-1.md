# V2 Cdn Endpoints Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2CdnEndpointsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `endpoint` | [`Endpoint`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/endpoint.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.endpoint import Endpoint
from digitaloceanapi.models.v_2_cdn_endpoints_response_1 import V2CdnEndpointsResponse1

v_2_cdn_endpoints_response_1 = V2CdnEndpointsResponse1(
    endpoint=Endpoint(
        origin='origin2',
        certificate_id='00001b94-0000-0000-0000-000000000000',
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        custom_domain='custom_domain6',
        endpoint='endpoint6',
        id='00001f7a-0000-0000-0000-000000000000',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



