# Home Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkhvbWVMb2NhdGlvbg

Location the Floating IP was created in. Routing is optimized for this Location.


# Class Name

`HomeLocation`


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
from hetznercloudapi.models.home_location import HomeLocation

home_location = HomeLocation(
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



