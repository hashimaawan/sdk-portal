# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Blocked` | `bool` | Required | Whether the IP is blocked |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Description` | `string` | Required | Description of the Resource |
| `DnsPtr` | [`List<DnsPtr>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `HomeLocation` | [`HomeLocation`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/home-location.md) | Required | Location the Floating IP was created in. Routing is optimized for this Location. |
| `Id` | `int` | Required | ID of the Resource |
| `Ip` | `string` | Required | IP address |
| `Labels` | `Dictionary<string, string>` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `Server` | `int?` | Required | ID of the Server the Floating IP is assigned to, null if it is not assigned at all |
| `Type` | [`Type16Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-16.md) | Required | Type of the Floating IP |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

FloatingIp floatingIp = new FloatingIp
{
    Blocked = false,
    Created = "2016-01-30T23:55:00+00:00",
    Description = "this describes my resource",
    DnsPtr = new List<DnsPtr>
    {
        new DnsPtr
        {
            DnsPtrProp = "server.example.com",
            Ip = "2001:db8::1",
        },
    },
    HomeLocation = new HomeLocation
    {
        City = "Falkenstein",
        Country = "DE",
        Description = "Falkenstein DC Park 1",
        Id = 1,
        Latitude = 50.47612,
        Longitude = 12.370071,
        Name = "fsn1",
        NetworkZone = "eu-central",
    },
    Id = 42,
    Ip = "131.232.99.1",
    Labels = new Dictionary<string, string>
    {
        ["key0"] = "labels6",
    },
    Name = "my-resource",
    Protection = new Protection
    {
        Delete = false,
    },
    Server = 42,
    Type = Type16Enum.Ipv4,
};
```



