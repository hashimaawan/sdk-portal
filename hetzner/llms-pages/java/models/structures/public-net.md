# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Enabled` | `boolean` | Required | Public Interface enabled or not | boolean getEnabled() | setEnabled(boolean enabled) |
| `Ipv4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/ipv-4.md) | Required | IP address (v4) | Ipv4 getIpv4() | setIpv4(Ipv4 ipv4) |
| `Ipv6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/ipv-6.md) | Required | IP address (v6) | Ipv6 getIpv6() | setIpv6(Ipv6 ipv6) |


# Example

```java
import cloud.hetzner.api.models.Ipv4;
import cloud.hetzner.api.models.Ipv6;
import cloud.hetzner.api.models.PublicNet;

PublicNet publicNet = new PublicNet.Builder(
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
.build();
```



