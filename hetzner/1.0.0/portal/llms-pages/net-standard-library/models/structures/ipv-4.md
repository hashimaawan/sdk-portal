# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer |
| `Ip` | `string` | Optional | IP address (v4) of this Load Balancer |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Ipv4 ipv4 = new Ipv4
{
    DnsPtr = "lb1.example.com",
    Ip = "1.2.3.4",
};
```



