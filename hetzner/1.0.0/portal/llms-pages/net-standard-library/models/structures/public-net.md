# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information


# Class Name

`PublicNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool` | Required | Public Interface enabled or not |
| `Ipv4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ipv-4.md) | Required | IP address (v4) |
| `Ipv6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ipv-6.md) | Required | IP address (v6) |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

PublicNet publicNet = new PublicNet
{
    Enabled = false,
    Ipv4 = new Ipv4
    {
        DnsPtr = "lb1.example.com",
        Ip = "1.2.3.4",
    },
    Ipv6 = new Ipv6
    {
        DnsPtr = "lb1.example.com",
        Ip = "2001:db8::1",
    },
};
```



