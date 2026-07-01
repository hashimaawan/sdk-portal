# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ


# Class Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Datacenters` | [`List<Datacenter>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/datacenter.md) | Required | - |
| `Recommendation` | `double` | Required | The Datacenter which is recommended to be used to create new Servers. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

DatacentersResponse datacentersResponse = new DatacentersResponse
{
    Datacenters = new List<Datacenter>
    {
        new Datacenter
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
    },
    Recommendation = 1,
};
```



