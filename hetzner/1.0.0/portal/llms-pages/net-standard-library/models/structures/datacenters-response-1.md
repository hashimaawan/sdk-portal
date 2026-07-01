# Datacenters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type object.*


# Class Name

`DatacentersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Datacenter` | [`Datacenter`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/datacenter.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

DatacentersResponse1 datacentersResponse1 = new DatacentersResponse1
{
    Datacenter = new Datacenter
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



