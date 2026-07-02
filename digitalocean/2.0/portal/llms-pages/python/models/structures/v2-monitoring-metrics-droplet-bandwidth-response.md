# V2 Monitoring Metrics Droplet Bandwidth Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBNZXRyaWNzJTI1MjBEcm9wbGV0JTI1MjBCYW5kd2lkdGglMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2MonitoringMetricsDropletBandwidthResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Data`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/data.md) | Required | - |
| `status` | [`Status13`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-13.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.data import Data
from digitaloceanapi.models.result import Result
from digitaloceanapi.models.status_13 import Status13
from digitaloceanapi.models.v_2_monitoring_metrics_droplet_bandwidth_response import V2MonitoringMetricsDropletBandwidthResponse

v_2_monitoring_metrics_droplet_bandwidth_response = V2MonitoringMetricsDropletBandwidthResponse(
    data=Data(
        result=[
            Result(
                metric={
                    'host_id': '19201920'
                },
                values=[
                    [
                        1435781430,
                        '1'
                    ],
                    [
                        1435781445,
                        '1'
                    ]
                ],
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    status=Status13.SUCCESS,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



