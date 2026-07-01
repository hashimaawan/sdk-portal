# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry

*This model accepts additional fields of type object.*


# Class Name

`Ipv64`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Blocked` | `bool` | Required | If the IP is blocked by our anti abuse dept |
| `DnsPtr` | [`List<DnsPtr8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default |
| `Id` | `int?` | Optional | ID of the Resource |
| `Ip` | `string` | Required | IP address (v6) of this Server |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

Ipv64 ipv64 = new Ipv64
{
    Blocked = false,
    DnsPtr = new List<DnsPtr8>
    {
        new DnsPtr8
        {
            DnsPtr = "server.example.com",
            Ip = "2001:db8::1",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Ip = "2001:db8::/64",
    Id = 42,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



