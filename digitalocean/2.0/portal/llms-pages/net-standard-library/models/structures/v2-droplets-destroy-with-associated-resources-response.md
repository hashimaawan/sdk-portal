# V2 Droplets Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/floating-ip.md) | Optional | - |
| `ReservedIps` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/floating-ip.md) | Optional | - |
| `Snapshots` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/floating-ip.md) | Optional | - |
| `VolumeSnapshots` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/floating-ip.md) | Optional | - |
| `Volumes` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/floating-ip.md) | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2DropletsDestroyWithAssociatedResourcesResponse v2DropletsDestroyWithAssociatedResourcesResponse = new V2DropletsDestroyWithAssociatedResourcesResponse
{
    FloatingIps = new List<FloatingIp>
    {
        new FloatingIp
        {
            Cost = "cost0",
            Id = "id2",
            Name = "name2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new FloatingIp
        {
            Cost = "cost0",
            Id = "id2",
            Name = "name2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ReservedIps = new List<FloatingIp>
    {
        new FloatingIp
        {
            Cost = "cost8",
            Id = "id0",
            Name = "name0",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Snapshots = new List<FloatingIp>
    {
        new FloatingIp
        {
            Cost = "cost0",
            Id = "id2",
            Name = "name2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new FloatingIp
        {
            Cost = "cost0",
            Id = "id2",
            Name = "name2",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    VolumeSnapshots = new List<FloatingIp>
    {
        new FloatingIp
        {
            Cost = "cost6",
            Id = "id8",
            Name = "name8",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Volumes = new List<FloatingIp>
    {
        new FloatingIp
        {
            Cost = "cost4",
            Id = "id6",
            Name = "name6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new FloatingIp
        {
            Cost = "cost4",
            Id = "id6",
            Name = "name6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



