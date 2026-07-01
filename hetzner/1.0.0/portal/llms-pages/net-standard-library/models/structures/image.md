# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdl


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BoundTo` | `int?` | Required | ID of Server the Image is bound to. Only set for Images of type `backup`. |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `CreatedFrom` | [`CreatedFrom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/created-from.md) | Required | Information about the Server the Image was created from |
| `Deleted` | `string` | Required | Point in time where the Image was deleted (in ISO-8601 format) |
| `Deprecated` | `string` | Required | Point in time when the Image is considered to be deprecated (in ISO-8601 format) |
| `Description` | `string` | Required | Description of the Image |
| `DiskSize` | `double` | Required | Size of the disk contained in the Image in GB |
| `Id` | `int` | Required | ID of the Resource |
| `ImageSize` | `double?` | Required | Size of the Image file in our storage in GB. For snapshot Images this is the value relevant for calculating costs for the Image. |
| `Labels` | `Dictionary<string, string>` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Unique identifier of the Image. This value is only set for system Images. |
| `OsFlavor` | [`OsFlavorEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/os-flavor.md) | Required | Flavor of operating system contained in the Image |
| `OsVersion` | `string` | Required | Operating system version |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `RapidDeploy` | `bool?` | Optional | Indicates that rapid deploy of the Image is available |
| `Status` | [`Status24Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/status-24.md) | Required | Whether the Image can be used or if it's still being created or unavailable |
| `Type` | [`Type22Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-22.md) | Required | Type of the Image |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

Image image = new Image
{
    BoundTo = null,
    Created = "2016-01-30T23:55:00+00:00",
    CreatedFrom = new CreatedFrom
    {
        Id = 1,
        Name = "Server",
    },
    Deleted = null,
    Deprecated = "2018-02-28T00:00:00+00:00",
    Description = "Ubuntu 20.04 Standard 64 bit",
    DiskSize = 10,
    Id = 42,
    ImageSize = 2.3,
    Labels = new Dictionary<string, string>
    {
        ["key0"] = "labels4",
    },
    Name = "ubuntu-20.04",
    OsFlavor = OsFlavorEnum.Ubuntu,
    OsVersion = "20.04",
    Protection = new Protection
    {
        Delete = false,
    },
    Status = Status24Enum.Unavailable,
    Type = Type22Enum.Snapshot,
    RapidDeploy = false,
};
```



