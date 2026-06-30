# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q


# Class Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Required | Hostname to set as a reverse DNS PTR entry | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Required | Public IP address for which the reverse DNS entry should be set | String getIp() | setIp(String ip) |


# Example

```java
import cloud.hetzner.api.models.ChangeLoadbalancerDnsPtrRequest;

ChangeLoadbalancerDnsPtrRequest changeLoadbalancerDnsPtrRequest = new ChangeLoadbalancerDnsPtrRequest.Builder(
    "lb1.example.com",
    "1.2.3.4"
)
.build();
```



