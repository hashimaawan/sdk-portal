# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Optional | IP address (v4) of this Load Balancer | String getIp() | setIp(String ip) |


# Example

```java
import cloud.hetzner.api.models.Ipv4;

Ipv4 ipv4 = new Ipv4.Builder()
    .dnsPtr("lb1.example.com")
    .ip("1.2.3.4")
    .build();
```



