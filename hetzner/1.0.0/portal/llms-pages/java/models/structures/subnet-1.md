# Subnet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlN1Ym5ldDE

*This model accepts additional fields of type Object.*


# Class Name

`Subnet1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IpRange` | `String` | Optional | Range to allocate IPs from. Must be a Subnet of the ip_range of the parent network object and must not overlap with any other subnets or with any destinations in routes. Minimum Network size is /30. We suggest that you pick a bigger Network with a /24 netmask. | String getIpRange() | setIpRange(String ipRange) |
| `NetworkZone` | `String` | Required | Name of Network zone. The Location object contains the `network_zone` property each Location belongs to. | String getNetworkZone() | setNetworkZone(String networkZone) |
| `Type` | [`Type42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-42.md) | Required | Type of Subnetwork | Type42 getType() | setType(Type42 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Subnet1;
import cloud.hetzner.api.models.Type42;
import java.io.IOException;

Subnet1 subnet1 = new Subnet1.Builder(
    "eu-central",
    Type42.VSWITCH
)
.ipRange("10.0.1.0/24")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



