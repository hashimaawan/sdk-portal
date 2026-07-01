# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRklwdjY

IP address (v6)


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer |
| `Ip` | `string` | Optional | IP address (v6) of this Load Balancer |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Ipv6 ipv6 = new Ipv6
{
    DnsPtr = "lb1.example.com",
    Ip = "2001:db8::1",
};
```



