# Load Balancers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Uy


# Class Name

`LoadBalancersResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancer` | [`LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/load-balancer.md) | Required | - | LoadBalancer getLoadBalancer() | setLoadBalancer(LoadBalancer loadBalancer) |


# Example

```java
import cloud.hetzner.api.models.Algorithm;
import cloud.hetzner.api.models.HealthStatus;
import cloud.hetzner.api.models.Http;
import cloud.hetzner.api.models.Ip;
import cloud.hetzner.api.models.Ipv4;
import cloud.hetzner.api.models.Ipv6;
import cloud.hetzner.api.models.LabelSelector7;
import cloud.hetzner.api.models.LoadBalancer;
import cloud.hetzner.api.models.LoadBalancerService;
import cloud.hetzner.api.models.LoadBalancerServiceHTTP;
import cloud.hetzner.api.models.LoadBalancerServiceHealthCheck;
import cloud.hetzner.api.models.LoadBalancerTarget;
import cloud.hetzner.api.models.LoadBalancerTargetServer;
import cloud.hetzner.api.models.LoadBalancerType;
import cloud.hetzner.api.models.LoadBalancersResponse2;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.Price;
import cloud.hetzner.api.models.PriceHourly;
import cloud.hetzner.api.models.PriceMonthly;
import cloud.hetzner.api.models.PrivateNet;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Protocol6Enum;
import cloud.hetzner.api.models.Protocol7Enum;
import cloud.hetzner.api.models.PublicNet;
import cloud.hetzner.api.models.Server11;
import cloud.hetzner.api.models.Status30Enum;
import cloud.hetzner.api.models.Target;
import cloud.hetzner.api.models.Type28Enum;
import cloud.hetzner.api.models.Type29Enum;
import java.util.Arrays;
import java.util.LinkedHashMap;

LoadBalancersResponse2 loadBalancersResponse2 = new LoadBalancersResponse2.Builder(
    new LoadBalancer.Builder(
        new Algorithm.Builder(
            Type28Enum.ROUND_ROBIN
        )
        .build(),
        "2016-01-30T23:55:00+00:00",
        42,
        10000,
        216,
        new LinkedHashMap<String, String>() {{
            put("key0", "labels2");
            put("key1", "labels1");
        }},
        new LoadBalancerType.Builder(
            "2016-01-30T23:50:00+00:00",
            "LB11",
            1D,
            10D,
            20000D,
            5D,
            25D,
            "lb11",
            Arrays.asList(
                new Price.Builder(
                    "fsn1",
                    new PriceHourly.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build(),
                    new PriceMonthly.Builder(
                        "1.1900000000000000",
                        "1.0000000000"
                    )
                    .build()
                )
                .build()
            )
        )
        .build(),
        new Location.Builder(
            "Falkenstein",
            "DE",
            "Falkenstein DC Park 1",
            1D,
            50.47612D,
            12.370071D,
            "fsn1",
            "eu-central"
        )
        .build(),
        "my-resource",
        42,
        Arrays.asList(
            new PrivateNet.Builder()
                .ip("10.0.0.2")
                .network(4711)
                .build()
        ),
        new Protection.Builder(
            false
        )
        .build(),
        new PublicNet.Builder(
            false,
            new Ipv4.Builder()
                .dnsPtr("lb1.example.com")
                .ip("1.2.3.4")
                .build(),
            new Ipv6.Builder()
                .dnsPtr("lb1.example.com")
                .ip("2001:db8::1")
                .build()
        )
        .build(),
        Arrays.asList(
            new LoadBalancerService.Builder(
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
            .build()
        ),
        Arrays.asList(
            new LoadBalancerTarget.Builder(
                Type29Enum.IP
            )
            .healthStatus(Arrays.asList(
                    new HealthStatus.Builder()
                        .listenPort(142)
                        .status(Status30Enum.UNKNOWN)
                        .build(),
                    new HealthStatus.Builder()
                        .listenPort(142)
                        .status(Status30Enum.UNKNOWN)
                        .build()
                ))
            .ip(new Ip.Builder(
                    "ip8"
                )
                .build())
            .labelSelector(new LabelSelector7.Builder(
                    "selector8"
                )
                .build())
            .server(new LoadBalancerTargetServer.Builder(
                    14
                )
                .build())
            .targets(Arrays.asList(
                    new Target.Builder()
                        .healthStatus(Arrays.asList(
                            new HealthStatus.Builder()
                                .listenPort(142)
                                .status(Status30Enum.UNKNOWN)
                                .build(),
                            new HealthStatus.Builder()
                                .listenPort(142)
                                .status(Status30Enum.UNKNOWN)
                                .build()
                        ))
                        .server(new Server11.Builder(
                            14
                        )
                        .build())
                        .type("type2")
                        .usePrivateIp(false)
                        .build(),
                    new Target.Builder()
                        .healthStatus(Arrays.asList(
                            new HealthStatus.Builder()
                                .listenPort(142)
                                .status(Status30Enum.UNKNOWN)
                                .build(),
                            new HealthStatus.Builder()
                                .listenPort(142)
                                .status(Status30Enum.UNKNOWN)
                                .build()
                        ))
                        .server(new Server11.Builder(
                            14
                        )
                        .build())
                        .type("type2")
                        .usePrivateIp(false)
                        .build(),
                    new Target.Builder()
                        .healthStatus(Arrays.asList(
                            new HealthStatus.Builder()
                                .listenPort(142)
                                .status(Status30Enum.UNKNOWN)
                                .build(),
                            new HealthStatus.Builder()
                                .listenPort(142)
                                .status(Status30Enum.UNKNOWN)
                                .build()
                        ))
                        .server(new Server11.Builder(
                            14
                        )
                        .build())
                        .type("type2")
                        .usePrivateIp(false)
                        .build()
                ))
            .build()
        )
    )
    .build()
)
.build();
```



