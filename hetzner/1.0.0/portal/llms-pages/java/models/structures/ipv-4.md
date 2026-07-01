# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)

*This model accepts additional fields of type Object.*


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Optional | IP address (v4) of this Load Balancer | String getIp() | setIp(String ip) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Ipv4;
import java.io.IOException;

Ipv4 ipv4 = new Ipv4.Builder()
    .dnsPtr("lb1.example.com")
    .ip("1.2.3.4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



