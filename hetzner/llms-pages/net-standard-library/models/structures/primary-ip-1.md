# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlByaW1hcnlJUDE


# Class Name

`PrimaryIP1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `int?` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all |
| `AssigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` |
| `AutoDelete` | `bool` | Required | Delete this Primary IP when the resource it is assigned to is deleted |
| `Blocked` | `bool` | Required | Whether the IP is blocked |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Datacenter` | [`Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at |
| `DnsPtr` | [`List<DnsPtr>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `Id` | `int` | Required | ID of the Resource |
| `Ip` | `string` | Required | IP address |
| `Labels` | `Dictionary<string, string>` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `Type` | [`Type50Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-50.md) | Required | Type of the Primary IP |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

PrimaryIP1 primaryIP1 = new PrimaryIP1
{
    AssigneeId = 17,
    AssigneeType = "server",
    AutoDelete = true,
    Blocked = false,
    Created = "2016-01-30T23:55:00+00:00",
    Datacenter = new Datacenter2
    {
        Description = "Falkenstein DC Park 8",
        Id = 42,
        Location = new Location
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
        Name = "fsn1-dc8",
        ServerTypes = new ServerTypes
        {
            Available = new List<double>
            {
                1,
                2,
                3,
            },
            AvailableForMigration = new List<double>
            {
                1,
                2,
                3,
            },
            Supported = new List<double>
            {
                1,
                2,
                3,
            },
        },
    },
    DnsPtr = new List<DnsPtr>
    {
        new DnsPtr
        {
            DnsPtrProp = "server.example.com",
            Ip = "2001:db8::1",
        },
    },
    Id = 42,
    Ip = "131.232.99.1",
    Labels = new Dictionary<string, string>
    {
        ["key0"] = "labels4",
        ["key1"] = "labels3",
    },
    Name = "my-resource",
    Protection = new Protection
    {
        Delete = false,
    },
    Type = Type50Enum.Ipv4,
};
```



