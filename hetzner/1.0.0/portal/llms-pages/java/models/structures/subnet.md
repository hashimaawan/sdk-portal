# Subnet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlN1Ym5ldA

*This model accepts additional fields of type Object.*


# Class Name

`Subnet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gateway` | `String` | Required | Gateway for Servers attached to this subnet. For subnets of type Server this is always the first IP of the network IP range. | String getGateway() | setGateway(String gateway) |
| `IpRange` | `String` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | String getIpRange() | setIpRange(String ipRange) |
| `NetworkZone` | `String` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | String getNetworkZone() | setNetworkZone(String networkZone) |
| `Type` | [`Type42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-42.md) | Required | Type of Subnetwork | Type42 getType() | setType(Type42 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Subnet;
import cloud.hetzner.api.models.Type42;
import java.io.IOException;

Subnet subnet = new Subnet.Builder(
    "10.0.0.1",
    "eu-central",
    Type42.SERVER
)
.ipRange("10.0.1.0/24")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



