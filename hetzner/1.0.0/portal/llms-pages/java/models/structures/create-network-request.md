# Create Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZU5ldHdvcmtSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`CreateNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpRange` | `String` | Required | IP range of the whole network which must span all included subnets. Must be one of the private IPv4 ranges of RFC1918. Minimum network size is /24. We highly recommend that you pick a larger network with a /16 netmask. | String getIpRange() | setIpRange(String ipRange) |
| `Labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) | Labels getLabels() | setLabels(Labels labels) |
| `Name` | `String` | Required | Name of the network | String getName() | setName(String name) |
| `Routes` | [`List<Route>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/route.md) | Optional | Array of routes set in this network. The destination of the route must be one of the private IPv4 ranges of RFC1918. The gateway must be a subnet/IP of the ip_range of the network object. The destination must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. The gateway cannot be the first IP of the networks ip_range and also cannot be 172.31.1.1. | List<Route> getRoutes() | setRoutes(List<Route> routes) |
| `Subnets` | [`List<Subnet1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/subnet-1.md) | Optional | Array of subnets allocated. | List<Subnet1> getSubnets() | setSubnets(List<Subnet1> subnets) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreateNetworkRequest;
import cloud.hetzner.api.models.Labels;
import cloud.hetzner.api.models.Route;
import cloud.hetzner.api.models.Subnet1;
import cloud.hetzner.api.models.Type42;
import java.io.IOException;
import java.util.Arrays;

CreateNetworkRequest createNetworkRequest = new CreateNetworkRequest.Builder(
    "10.0.0.0/16",
    "mynet"
)
.labels(new Labels.Builder()
        .labelkey("labelkey4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.routes(Arrays.asList(
        new Route.Builder(
            "destination8",
            "gateway6"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.subnets(Arrays.asList(
        new Subnet1.Builder(
            "network_zone2",
            Type42.CLOUD
        )
        .ipRange("ip_range6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Subnet1.Builder(
            "network_zone2",
            Type42.CLOUD
        )
        .ipRange("ip_range6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Subnet1.Builder(
            "network_zone2",
            Type42.CLOUD
        )
        .ipRange("ip_range6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



