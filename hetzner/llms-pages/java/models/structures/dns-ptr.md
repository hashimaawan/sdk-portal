# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkRuc1B0cg


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Required | DNS pointer for the specific IP address | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Required | Single IPv4 or IPv6 address | String getIp() | setIp(String ip) |


# Example

```java
import cloud.hetzner.api.models.DnsPtr;

DnsPtr dnsPtr = new DnsPtr.Builder(
    "server.example.com",
    "2001:db8::1"
)
.build();
```



