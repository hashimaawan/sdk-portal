# Location 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkxvY2F0aW9uMTY

Location of the Volume. Volume can only be attached to Servers in the same Location.


# Class Name

`Location16`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `str` | Required | City the Location is closest to |
| `country` | `str` | Required | ISO 3166-1 alpha-2 code of the country the Location resides in |
| `description` | `str` | Required | Description of the Location |
| `id` | `float` | Required | ID of the Location |
| `latitude` | `float` | Required | Latitude of the city closest to the Location |
| `longitude` | `float` | Required | Longitude of the city closest to the Location |
| `name` | `str` | Required | Unique identifier of the Location |
| `network_zone` | `str` | Required | Name of network zone this Location resides in |


# Example

```python
from hetznercloudapi.models.location_16 import Location16

location_16 = Location16(
    city='Falkenstein',
    country='DE',
    description='Falkenstein DC Park 1',
    id=1,
    latitude=50.47612,
    longitude=12.370071,
    name='fsn1',
    network_zone='eu-central'
)
```



