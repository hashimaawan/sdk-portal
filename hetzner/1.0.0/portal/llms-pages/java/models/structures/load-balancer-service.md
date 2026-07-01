# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DestinationPort` | `int` | Required | Port the Load Balancer will balance to | int getDestinationPort() | setDestinationPort(int destinationPort) |
| `HealthCheck` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-service-health-check.md) | Required | Service health check | LoadBalancerServiceHealthCheck getHealthCheck() | setHealthCheck(LoadBalancerServiceHealthCheck healthCheck) |
| `Http` | [`LoadBalancerServiceHttp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https | LoadBalancerServiceHttp getHttp() | setHttp(LoadBalancerServiceHttp http) |
| `ListenPort` | `int` | Required | Port the Load Balancer listens on | int getListenPort() | setListenPort(int listenPort) |
| `Protocol` | [`Protocol7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer | Protocol7 getProtocol() | setProtocol(Protocol7 protocol) |
| `Proxyprotocol` | `boolean` | Required | Is Proxyprotocol enabled or not | boolean getProxyprotocol() | setProxyprotocol(boolean proxyprotocol) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Http;
import cloud.hetzner.api.models.LoadBalancerService;
import cloud.hetzner.api.models.LoadBalancerServiceHealthCheck;
import cloud.hetzner.api.models.LoadBalancerServiceHttp;
import cloud.hetzner.api.models.Protocol6;
import cloud.hetzner.api.models.Protocol7;
import java.io.IOException;
import java.util.Arrays;

LoadBalancerService loadBalancerService = new LoadBalancerService.Builder(
    80,
    new LoadBalancerServiceHealthCheck.Builder(
        15,
        4711,
        Protocol6.HTTP,
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
    Protocol7.HTTPS,
    false
)
.http(new LoadBalancerServiceHttp.Builder()
        .certificates(Arrays.asList(
            180
        ))
        .cookieLifetime(160)
        .cookieName("cookie_name6")
        .redirectHttp(false)
        .stickySessions(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



