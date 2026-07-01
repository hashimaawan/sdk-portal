# Load Balancer Service Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIZWFsdGhDaGVjaw

Service health check


# Class Name

`LoadBalancerServiceHealthCheck`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Http` | [`Http`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/http.md) | Optional | Additional configuration for protocol http | Http getHttp() | setHttp(Http http) |
| `Interval` | `int` | Required | Time interval in seconds health checks are performed | int getInterval() | setInterval(int interval) |
| `Port` | `int` | Required | Port the health check will be performed on | int getPort() | setPort(int port) |
| `Protocol` | [`Protocol6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/protocol-6.md) | Required | Type of the health check | Protocol6Enum getProtocol() | setProtocol(Protocol6Enum protocol) |
| `Retries` | `int` | Required | Unsuccessful retries needed until a target is considered unhealthy; an unhealthy target needs the same number of successful retries to become healthy again | int getRetries() | setRetries(int retries) |
| `Timeout` | `int` | Required | Time in seconds after an attempt is considered a timeout | int getTimeout() | setTimeout(int timeout) |


# Example

```java
import cloud.hetzner.api.models.Http;
import cloud.hetzner.api.models.LoadBalancerServiceHealthCheck;
import cloud.hetzner.api.models.Protocol6Enum;
import java.util.Arrays;

LoadBalancerServiceHealthCheck loadBalancerServiceHealthCheck = new LoadBalancerServiceHealthCheck.Builder(
    15,
    4711,
    Protocol6Enum.HTTP,
    3,
    10
)
.http(new Http.Builder(
        "domain4",
        "path2"
    )
    .response("response8")
    .statusCodes(Arrays.asList(
            "status_codes0",
            "status_codes1",
            "status_codes2"
        ))
    .tls(false)
    .build())
.build();
```



