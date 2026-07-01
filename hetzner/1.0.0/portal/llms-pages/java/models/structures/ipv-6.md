# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRklwdjY

IP address (v6)

*This model accepts additional fields of type Object.*


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Optional | IP address (v6) of this Load Balancer | String getIp() | setIp(String ip) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Ipv6;
import java.io.IOException;

Ipv6 ipv6 = new Ipv6.Builder()
    .dnsPtr("lb1.example.com")
    .ip("2001:db8::1")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



