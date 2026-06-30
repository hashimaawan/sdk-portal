# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl


# Class Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `Volumes` | [`List<Volume1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/volume-1.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

VolumesResponse volumesResponse = new VolumesResponse
{
    Volumes = new List<Volume1>
    {
        new Volume1
        {
            Created = "2016-01-30T23:55:00+00:00",
            Format = "xfs",
            Id = 42,
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels4",
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
        },
    },
    Meta = new Meta
    {
        Pagination = new Pagination
        {
            LastPage = 77.7,
            NextPage = 209.18,
            Page = 17.58,
            PerPage = 13.34,
            PreviousPage = 50.02,
            TotalEntries = 206.64,
        },
    },
};
```



