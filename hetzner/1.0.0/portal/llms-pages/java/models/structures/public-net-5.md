# Public Net 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlB1YmxpY05ldDU

Public Network options

*This model accepts additional fields of type Object.*


# Class Name

`PublicNet5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EnableIpv4` | `Boolean` | Optional | Attach an IPv4 on the public NIC. If false, no IPv4 address will be attached. Defaults to true. | Boolean getEnableIpv4() | setEnableIpv4(Boolean enableIpv4) |
| `EnableIpv6` | `Boolean` | Optional | Attach an IPv6 on the public NIC. If false, no IPv6 address will be attached. Defaults to true. | Boolean getEnableIpv6() | setEnableIpv6(Boolean enableIpv6) |
| `Ipv4` | `Integer` | Optional | ID of the ipv4 Primary IP to use. If omitted and enable_ipv4 is true, a new ipv4 Primary IP will automatically be created. | Integer getIpv4() | setIpv4(Integer ipv4) |
| `Ipv6` | `Integer` | Optional | ID of the ipv6 Primary IP to use. If omitted and enable_ipv6 is true, a new ipv6 Primary IP will automatically be created. | Integer getIpv6() | setIpv6(Integer ipv6) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.PublicNet5;
import java.io.IOException;

PublicNet5 publicNet5 = new PublicNet5.Builder()
    .enableIpv4(false)
    .enableIpv6(false)
    .ipv4(42)
    .ipv6(102)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



