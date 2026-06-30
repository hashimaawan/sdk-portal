# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DestinationPort` | `int` | Required | Port the Load Balancer will balance to | int getDestinationPort() | setDestinationPort(int destinationPort) |
| `HealthCheck` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancer-service-health-check.md) | Required | Service health check | LoadBalancerServiceHealthCheck getHealthCheck() | setHealthCheck(LoadBalancerServiceHealthCheck healthCheck) |
| `Http` | [`LoadBalancerServiceHTTP`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https | LoadBalancerServiceHTTP getHttp() | setHttp(LoadBalancerServiceHTTP http) |
| `ListenPort` | `int` | Required | Port the Load Balancer listens on | int getListenPort() | setListenPort(int listenPort) |
| `Protocol` | [`Protocol7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer | Protocol7Enum getProtocol() | setProtocol(Protocol7Enum protocol) |
| `Proxyprotocol` | `boolean` | Required | Is Proxyprotocol enabled or not | boolean getProxyprotocol() | setProxyprotocol(boolean proxyprotocol) |


# Example

```java
import cloud.hetzner.api.models.Http;
import cloud.hetzner.api.models.LoadBalancerService;
import cloud.hetzner.api.models.LoadBalancerServiceHTTP;
import cloud.hetzner.api.models.LoadBalancerServiceHealthCheck;
import cloud.hetzner.api.models.Protocol6Enum;
import cloud.hetzner.api.models.Protocol7Enum;
import java.util.Arrays;

LoadBalancerService loadBalancerService = new LoadBalancerService.Builder(
    80,
    new LoadBalancerServiceHealthCheck.Builder(
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
    .build(),
    443,
    Protocol7Enum.HTTPS,
    false
)
.http(new LoadBalancerServiceHTTP.Builder()
        .certificates(Arrays.asList(
            180
        ))
        .cookieLifetime(160)
        .cookieName("cookie_name6")
        .redirectHttp(false)
        .stickySessions(false)
        .build())
.build();
```



