# Health Check 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkhlYWx0aENoZWNrMQ

An object specifying health check settings for the load balancer.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`HealthCheck1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `check_interval_seconds` | `int` | Optional | The number of seconds between between two consecutive health checks.<br><br>**Default**: `10` |
| `healthy_threshold` | `int` | Optional | The number of times a health check must pass for a backend Droplet to be marked "healthy" and be re-added to the pool.<br><br>**Default**: `3` |
| `path` | `str` | Optional | The path on the backend Droplets to which the load balancer instance will send a request.<br><br>**Default**: `"/"` |
| `port` | `int` | Optional | An integer representing the port on the backend Droplets on which the health check will attempt a connection.<br><br>**Default**: `80` |
| `protocol` | [`Protocol1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/protocol-1.md) | Optional | The protocol used for health checks sent to the backend Droplets. The possible values are `http`, `https`, or `tcp`.<br><br>**Default**: `"http"` |
| `response_timeout_seconds` | `int` | Optional | The number of seconds the load balancer instance will wait for a response until marking a health check as failed.<br><br>**Default**: `5` |
| `unhealthy_threshold` | `int` | Optional | The number of times a health check must fail for a backend Droplet to be marked "unhealthy" and be removed from the pool.<br><br>**Default**: `5` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.health_check_1 import HealthCheck1
from digitaloceanapi.models.protocol_1 import Protocol1

health_check_1 = HealthCheck1(
    check_interval_seconds=10,
    healthy_threshold=3,
    path='/',
    port=80,
    protocol=Protocol1.HTTP,
    response_timeout_seconds=5,
    unhealthy_threshold=5,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



