# Datacenter 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFjZW50ZXI2

Datacenter this Resource is located at


# Class Name

`Datacenter6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Required | Description of the Datacenter |
| `Id` | `int` | Required | ID of the Resource |
| `Location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/location.md) | Required | - |
| `Name` | `string` | Required | Unique identifier of the Datacenter |
| `ServerTypes` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-types.md) | Required | The Server types the Datacenter can handle |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

Datacenter6 datacenter6 = new Datacenter6
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
};
```



