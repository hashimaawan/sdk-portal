# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Any.*


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/location.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.location import Location
from hetznercloudapi.models.locations_response_1 import LocationsResponse1

locations_response_1 = LocationsResponse1(
    location=Location(
        city='Falkenstein',
        country='DE',
        description='Falkenstein DC Park 1',
        id=1,
        latitude=50.47612,
        longitude=12.370071,
        name='fsn1',
        network_zone='eu-central',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



