# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRklwdjY

IP address (v6)


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Optional | IP address (v6) of this Load Balancer | String getIp() | setIp(String ip) |


# Example

```java
import cloud.hetzner.api.models.Ipv6;

Ipv6 ipv6 = new Ipv6.Builder()
    .dnsPtr("lb1.example.com")
    .ip("2001:db8::1")
    .build();
```



