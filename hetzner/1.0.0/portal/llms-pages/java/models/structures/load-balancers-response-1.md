# Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Required | - | Action getAction() | setAction(Action action) |
| `LoadBalancer` | [`LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer.md) | Required | - | LoadBalancer getLoadBalancer() | setLoadBalancer(LoadBalancer loadBalancer) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Algorithm;
import cloud.hetzner.api.models.Error;
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
import cloud.hetzner.api.models.LoadBalancersResponse1;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.Price;
import cloud.hetzner.api.models.PriceHourly;
import cloud.hetzner.api.models.PriceMonthly;
import cloud.hetzner.api.models.PrivateNet;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Protocol6;
import cloud.hetzner.api.models.Protocol7;
import cloud.hetzner.api.models.PublicNet;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Server11;
import cloud.hetzner.api.models.Status;
import cloud.hetzner.api.models.Status30;
import cloud.hetzner.api.models.Target;
import cloud.hetzner.api.models.Type28;
import cloud.hetzner.api.models.Type29;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

LoadBalancersResponse1 loadBalancersResponse1 = new LoadBalancersResponse1.Builder(
    new Action.Builder(
        "start_server",
        new Error.Builder(
            "action_failed",
            "Action failed"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "2016-01-30T23:55:00+00:00",
        42,
        100D,
        Arrays.asList(
            new Resource.Builder(
                42,
                "server"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "2016-01-30T23:55:00+00:00",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new LoadBalancer.Builder(
        new Algorithm.Builder(
            Type28.ROUND_ROBIN
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
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
        42,
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
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



