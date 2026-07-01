# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type object.*


# Class Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/volume-1.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

VolumesResponse2 volumesResponse2 = new VolumesResponse2
{
    Volume = new Volume1
    {
        Created = "2016-01-30T23:55:00+00:00",
        Format = "xfs",
        Id = 42,
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels8",
            ["key1"] = "labels9",
            ["key2"] = "labels0",
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Name = "my-resource",
        Protection = new Protection
        {
            Delete = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        Server = 12,
        Size = 42,
        Status = Status113.Available,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



