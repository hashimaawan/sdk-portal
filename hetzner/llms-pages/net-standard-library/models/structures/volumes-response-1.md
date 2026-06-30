# Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `NextActions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Required | - |
| `Volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/volume-1.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

VolumesResponse1 volumesResponse1 = new VolumesResponse1
{
    Action = new Action
    {
        Command = "start_server",
        Error = new Error
        {
            Code = "action_failed",
            Message = "Action failed",
        },
        Finished = "2016-01-30T23:55:00+00:00",
        Id = 42,
        Progress = 100,
        Resources = new List<Resource>
        {
            new Resource
            {
                Id = 42,
                Type = "server",
            },
        },
        Started = "2016-01-30T23:55:00+00:00",
        Status = StatusEnum.Running,
    },
    NextActions = new List<Action>
    {
        new Action
        {
            Command = "start_server",
            Error = new Error
            {
                Code = "action_failed",
                Message = "Action failed",
            },
            Finished = "2016-01-30T23:55:00+00:00",
            Id = 42,
            Progress = 100,
            Resources = new List<Resource>
            {
                new Resource
                {
                    Id = 42,
                    Type = "server",
                },
            },
            Started = "2016-01-30T23:55:00+00:00",
            Status = StatusEnum.Success,
        },
    },
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
};
```



