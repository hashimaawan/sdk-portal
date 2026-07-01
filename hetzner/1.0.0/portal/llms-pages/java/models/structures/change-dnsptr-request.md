# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q


# Class Name

`ChangeDNSPTRRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DnsPtr` | `String` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` | String getDnsPtr() | setDnsPtr(String dnsPtr) |
| `Ip` | `String` | Required | IP address for which to set the reverse DNS entry | String getIp() | setIp(String ip) |


# Example

```java
import cloud.hetzner.api.models.ChangeDNSPTRRequest;

ChangeDNSPTRRequest changeDNSPTRRequest = new ChangeDNSPTRRequest.Builder(
    "server02.example.com",
    "1.2.3.4"
)
.build();
```



