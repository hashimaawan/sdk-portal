# Locations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2U


# Class Name

`LocationsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `locations` | [`List[Location]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/location.md) | Required | - |


# Example

```python
from hetznercloudapi.models.location import Location
from hetznercloudapi.models.locations_response import LocationsResponse

locations_response = LocationsResponse(
    locations=[
        Location(
            city='Falkenstein',
            country='DE',
            description='Falkenstein DC Park 1',
            id=1,
            latitude=50.47612,
            longitude=12.370071,
            name='fsn1',
            network_zone='eu-central'
        )
    ]
)
```



