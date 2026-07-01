# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/algorithm.md) | Required | Algorithm of the Load Balancer | Algorithm getAlgorithm() | setAlgorithm(Algorithm algorithm) |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `IncludedTraffic` | `int` | Required | Free Traffic for the current billing period in bytes | int getIncludedTraffic() | setIncludedTraffic(int includedTraffic) |
| `IngoingTraffic` | `Integer` | Required | Inbound Traffic for the current billing period in bytes | Integer getIngoingTraffic() | setIngoingTraffic(Integer ingoingTraffic) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `LoadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-type.md) | Required | - | LoadBalancerType getLoadBalancerType() | setLoadBalancerType(LoadBalancerType loadBalancerType) |
| `Location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/location.md) | Required | - | Location getLocation() | setLocation(Location location) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `OutgoingTraffic` | `Integer` | Required | Outbound Traffic for the current billing period in bytes | Integer getOutgoingTraffic() | setOutgoingTraffic(Integer outgoingTraffic) |
| `PrivateNet` | [`List<PrivateNet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/private-net.md) | Required | Private networks information | List<PrivateNet> getPrivateNet() | setPrivateNet(List<PrivateNet> privateNet) |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/protection.md) | Required | Protection configuration for the Resource | Protection getProtection() | setProtection(Protection protection) |
| `PublicNet` | [`PublicNet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/public-net.md) | Required | Public network information | PublicNet getPublicNet() | setPublicNet(PublicNet publicNet) |
| `Services` | [`List<LoadBalancerService>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-service.md) | Required | List of services that belong to this Load Balancer | List<LoadBalancerService> getServices() | setServices(List<LoadBalancerService> services) |
| `Targets` | [`List<LoadBalancerTarget>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-target.md) | Required | List of targets that belong to this Load Balancer | List<LoadBalancerTarget> getTargets() | setTargets(List<LoadBalancerTarget> targets) |
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
import cloud.hetzner.api.models.Location;
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

LoadBalancer loadBalancer = new LoadBalancer.Builder(
    new Algorithm.Builder(
        Type28.ROUND_ROBIN
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    "2016-01-30T23:55:00+00:00",
    42,
    10000,
    210,
    new LinkedHashMap<String, String>() {{
        put("key0", "labels8");
        put("key1", "labels7");
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
    36,
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
.build();
```



