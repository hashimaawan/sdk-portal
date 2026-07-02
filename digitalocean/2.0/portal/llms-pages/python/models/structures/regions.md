# Regions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlZ2lvbnM

A map of region to regional state

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Regions`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `eu_west` | [`EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/eu-west.md) | Optional | - |
| `us_east` | [`EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/eu-west.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.eu_west import EuWest
from digitaloceanapi.models.regions import Regions
from digitaloceanapi.models.status_16 import Status16

regions = Regions(
    eu_west=EuWest(
        status=Status16.DOWN,
        status_changed_at='status_changed_at4',
        thirty_day_uptime_percentage=227.78,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    us_east=EuWest(
        status=Status16.DOWN,
        status_changed_at='status_changed_at4',
        thirty_day_uptime_percentage=121.56,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



