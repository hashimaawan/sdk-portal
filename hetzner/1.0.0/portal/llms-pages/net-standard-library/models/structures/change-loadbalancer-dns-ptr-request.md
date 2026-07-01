# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q


# Class Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | Hostname to set as a reverse DNS PTR entry |
| `Ip` | `string` | Required | Public IP address for which the reverse DNS entry should be set |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ChangeLoadbalancerDnsPtrRequest changeLoadbalancerDnsPtrRequest = new ChangeLoadbalancerDnsPtrRequest
{
    DnsPtr = "lb1.example.com",
    Ip = "1.2.3.4",
};
```



