# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlJvdXRl

*This model accepts additional fields of type Object.*


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Destination` | `String` | Required | Destination network or host of this route. Must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. Must be one of the private IPv4 ranges of RFC1918. | String getDestination() | setDestination(String destination) |
| `Gateway` | `String` | Required | Gateway for the route. Cannot be the first IP of the networks ip_range and also cannot be 172.31.1.1 as this IP is being used as a gateway for the public network interface of Servers. | String getGateway() | setGateway(String gateway) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Route;
import java.io.IOException;

Route route = new Route.Builder(
    "10.100.1.0/24",
    "10.0.1.1"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



