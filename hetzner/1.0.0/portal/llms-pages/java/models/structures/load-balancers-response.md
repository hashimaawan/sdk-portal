# Load Balancers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LoadBalancers` | [`List<LoadBalancer>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer.md) | Required | - | List<LoadBalancer> getLoadBalancers() | setLoadBalancers(List<LoadBalancer> loadBalancers) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Algorithm;
import cloud.hetzner.api.models.HealthStatus;
import cloud.hetzner.api.models.Http;
import cloud.hetzner.api.models.Ip;
import cloud.hetzner.api.models.Ipv4;
import cloud.hetzner.api.models.Ipv6;
import cloud.hetzner.api.models.LabelSelector7;
import cloud.hetzner.api.models.LoadBalancer;
import cloud.hetzner.api.models.LoadBalancerService;
import cloud.hetzner.api.models.LoadBalancerServiceHealthCheck;
import cloud.hetzner.api.models.LoadBalancerServiceHttp;
import cloud.hetzner.api.models.LoadBalancerTarget;
import cloud.hetzner.api.models.LoadBalancerTargetServer;
import cloud.hetzner.api.models.LoadBalancerType;
import cloud.hetzner.api.models.LoadBalancersResponse;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Price;
import cloud.hetzner.api.models.PriceHourly;
import cloud.hetzner.api.models.PriceMonthly;
import cloud.hetzner.api.models.PrivateNet;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Protocol6;
import cloud.hetzner.api.models.Protocol7;
import cloud.hetzner.api.models.PublicNet;
import cloud.hetzner.api.models.Server11;
import cloud.hetzner.api.models.Status30;
import cloud.hetzner.api.models.Target;
import cloud.hetzner.api.models.Type28;
import cloud.hetzner.api.models.Type29;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

LoadBalancersResponse loadBalancersResponse = new LoadBalancersResponse.Builder(
    Arrays.asList(
        new LoadBalancer.Builder(
            new Algorithm.Builder(
                Type28.ROUND_ROBIN
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "2016-01-30T23:55:00+00:00",
            42,
            10000,
            204,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels8");
                put("key1", "labels7");
                put("key2", "labels6");
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
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build(),
                        new PriceMonthly.Builder(
                            "1.1900000000000000",
                            "1.0000000000"
                        )
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                        .build()
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
                )
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            "my-resource",
            30,
            Arrays.asList(
                new PrivateNet.Builder()
                    .ip("10.0.0.2")
                    .network(4711)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ),
            new Protection.Builder(
                false
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new PublicNet.Builder(
                false,
                new Ipv4.Builder()
                    .dnsPtr("lb1.example.com")
                    .ip("1.2.3.4")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new Ipv6.Builder()
                    .dnsPtr("lb1.example.com")
                    .ip("2001:db8::1")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            Arrays.asList(
                new LoadBalancerService.Builder(
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
                .build()
            ),
            Arrays.asList(
                new LoadBalancerTarget.Builder(
                    Type29.IP
                )
                .healthStatus(Arrays.asList(
                        new HealthStatus.Builder()
                            .listenPort(142)
                            .status(Status30.UNKNOWN)
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build(),
                        new HealthStatus.Builder()
                            .listenPort(142)
                            .status(Status30.UNKNOWN)
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build()
                    ))
                .ip(new Ip.Builder(
                        "ip8"
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .labelSelector(new LabelSelector7.Builder(
                        "selector8"
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .server(new LoadBalancerTargetServer.Builder(
                        14
                    )
                    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build())
                .targets(Arrays.asList(
                        new Target.Builder()
                            .healthStatus(Arrays.asList(
                                new HealthStatus.Builder()
                                    .listenPort(142)
                                    .status(Status30.UNKNOWN)
                                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                                    .build(),
                                new HealthStatus.Builder()
                                    .listenPort(142)
                                    .status(Status30.UNKNOWN)
                                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                                    .build()
                            ))
                            .server(new Server11.Builder(
                                14
                            )
                            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build())
                            .type("type2")
                            .usePrivateIp(false)
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build(),
                        new Target.Builder()
                            .healthStatus(Arrays.asList(
                                new HealthStatus.Builder()
                                    .listenPort(142)
                                    .status(Status30.UNKNOWN)
                                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                                    .build(),
                                new HealthStatus.Builder()
                                    .listenPort(142)
                                    .status(Status30.UNKNOWN)
                                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                                    .build()
                            ))
                            .server(new Server11.Builder(
                                14
                            )
                            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build())
                            .type("type2")
                            .usePrivateIp(false)
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build(),
                        new Target.Builder()
                            .healthStatus(Arrays.asList(
                                new HealthStatus.Builder()
                                    .listenPort(142)
                                    .status(Status30.UNKNOWN)
                                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                                    .build(),
                                new HealthStatus.Builder()
                                    .listenPort(142)
                                    .status(Status30.UNKNOWN)
                                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                                    .build()
                            ))
                            .server(new Server11.Builder(
                                14
                            )
                            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build())
                            .type("type2")
                            .usePrivateIp(false)
                        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                            .build()
                    ))
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
            )
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.meta(new Meta.Builder(
        new Pagination.Builder(
            77.7D,
            209.18D,
            17.58D,
            13.34D,
            50.02D,
            206.64D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



