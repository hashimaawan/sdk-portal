# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkRuc1B0cjg


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Required | DNS pointer for the specific IP address | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up | String getIp() | setIp(String ip) |


# Example

```java
import cloud.hetzner.api.models.DnsPtr8;

DnsPtr8 dnsPtr8 = new DnsPtr8.Builder(
    "server.example.com",
    "2001:db8::1"
)
.build();
```



