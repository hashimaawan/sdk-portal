# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRk5ldHdvcms

*This model accepts additional fields of type Object.*


# Class Name

`Network`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Created` | `String` | Required | Point in time when the Network was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Id` | `int` | Required | ID of the Network | int getId() | setId(int id) |
| `IpRange` | `String` | Required | IPv4 prefix of the whole Network | String getIpRange() | setIpRange(String ipRange) |
| `Labels` | `Object` | Required | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `LoadBalancers` | `List<Integer>` | Optional | Array of IDs of Load Balancers attached to this Network | List<Integer> getLoadBalancers() | setLoadBalancers(List<Integer> loadBalancers) |
| `Name` | `String` | Required | Name of the Network | String getName() | setName(String name) |
| `Protection` | [`Protection11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/protection-11.md) | Required | Protection configuration for the Network | Protection11 getProtection() | setProtection(Protection11 protection) |
| `Routes` | [`List<Route>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/route.md) | Required | Array of routes set in this Network | List<Route> getRoutes() | setRoutes(List<Route> routes) |
| `Servers` | `List<Integer>` | Required | Array of IDs of Servers attached to this Network | List<Integer> getServers() | setServers(List<Integer> servers) |
| `Subnets` | [`List<Subnet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/subnet.md) | Required | Array subnets allocated in this Network | List<Subnet> getSubnets() | setSubnets(List<Subnet> subnets) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Network;
import cloud.hetzner.api.models.Protection11;
import cloud.hetzner.api.models.Route;
import cloud.hetzner.api.models.Subnet;
import cloud.hetzner.api.models.Type42;
import java.io.IOException;
import java.util.Arrays;

Network network = new Network.Builder(
    "2016-01-30T23:50:00+00:00",
    4711,
    "10.0.0.0/16",
    ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    "mynet",
    new Protection11.Builder(
        false
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    Arrays.asList(
        new Route.Builder(
            "10.100.1.0/24",
            "10.0.1.1"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Arrays.asList(
        42
    ),
    Arrays.asList(
        new Subnet.Builder(
            "10.0.0.1",
            "eu-central",
            Type42.CLOUD
        )
        .ipRange("10.0.1.0/24")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.loadBalancers(Arrays.asList(
        42
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



