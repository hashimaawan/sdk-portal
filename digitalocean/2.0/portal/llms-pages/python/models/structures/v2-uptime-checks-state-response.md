# V2 Uptime Checks State Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwU3RhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2UptimeChecksStateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`State3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/state-3.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.eu_west import EuWest
from digitaloceanapi.models.previous_outage import PreviousOutage
from digitaloceanapi.models.regions import Regions
from digitaloceanapi.models.state_3 import State3
from digitaloceanapi.models.status_16 import Status16
from digitaloceanapi.models.v_2_uptime_checks_state_response import V2UptimeChecksStateResponse

v_2_uptime_checks_state_response = V2UptimeChecksStateResponse(
    state=State3(
        previous_outage=PreviousOutage(
            duration_seconds=16,
            ended_at='ended_at4',
            region='region8',
            started_at='started_at4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        regions=Regions(
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



