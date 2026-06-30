# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZTE


# Class Name

`Volume1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Format` | `string` | Required | Filesystem of the Volume if formatted on creation, null if not formatted on creation |
| `Id` | `int` | Required | ID of the Resource |
| `Labels` | `Dictionary<string, string>` | Required | User-defined labels (key-value pairs) |
| `LinuxDevice` | `string` | Required | Device path on the file system for the Volume |
| `Location` | [`Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `Server` | `int?` | Required | ID of the Server the Volume is attached to, null if it is not attached at all |
| `Size` | `double` | Required | Size in GB of the Volume |
| `Status` | [`Status113Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/status-113.md) | Required | Current status of the Volume |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

Volume1 volume1 = new Volume1
{
    Created = "2016-01-30T23:55:00+00:00",
    Format = "xfs",
    Id = 42,
    Labels = new Dictionary<string, string>
    {
        ["key0"] = "labels8",
    },
    LinuxDevice = "/dev/disk/by-id/scsi-0HC_Volume_4711",
    Location = new Location16
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
    Name = "my-resource",
    Protection = new Protection
    {
        Delete = false,
    },
    Server = 12,
    Size = 42,
    Status = Status113Enum.Available,
};
```



