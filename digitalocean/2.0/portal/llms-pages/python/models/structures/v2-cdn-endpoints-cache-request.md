# V2 Cdn Endpoints Cache Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwQ2FjaGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2CdnEndpointsCacheRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `files` | `List[str]` | Required | An array of strings containing the path to the content to be purged from the CDN cache. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.v_2_cdn_endpoints_cache_request import V2CdnEndpointsCacheRequest

v_2_cdn_endpoints_cache_request = V2CdnEndpointsCacheRequest(
    files=[
        'path/to/image.png',
        'path/to/css/*'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



