# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action.md) | Optional | - |
| `Image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ServersActionsCreateImageResponse serversActionsCreateImageResponse = new ServersActionsCreateImageResponse
{
    Action = new Action
    {
        Command = "command6",
        Error = new Error
        {
            Code = "code2",
            Message = "message4",
        },
        Finished = "finished0",
        Id = 238,
        Progress = 143.26,
        Resources = new List<Resource>
        {
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
        },
        Started = "started8",
        Status = StatusEnum.Running,
    },
    Image = new Image
    {
        BoundTo = 186,
        Created = "created6",
        CreatedFrom = new CreatedFrom
        {
            Id = 60,
            Name = "name6",
        },
        Deleted = "deleted4",
        Deprecated = "deprecated8",
        Description = "description6",
        DiskSize = 244.18,
        Id = 128,
        ImageSize = 141.34,
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels4",
        },
        Name = "name6",
        OsFlavor = OsFlavorEnum.Debian,
        OsVersion = "os_version4",
        Protection = new Protection
        {
            Delete = false,
        },
        Status = Status24Enum.Unavailable,
        Type = Type22Enum.App,
        RapidDeploy = false,
    },
};
```



