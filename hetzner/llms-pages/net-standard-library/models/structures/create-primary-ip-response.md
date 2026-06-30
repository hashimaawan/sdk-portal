# Create Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlc3BvbnNl


# Class Name

`CreatePrimaryIPResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Optional | - |
| `PrimaryIp` | [`PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/primary-ip-1.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

CreatePrimaryIPResponse createPrimaryIPResponse = new CreatePrimaryIPResponse
{
    PrimaryIp = new PrimaryIP1
    {
        AssigneeId = 17,
        AssigneeType = "server",
        AutoDelete = true,
        Blocked = false,
        Created = "2016-01-30T23:55:00+00:00",
        Datacenter = new Datacenter2
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
        DnsPtr = new List<DnsPtr>
        {
            new DnsPtr
            {
                DnsPtrProp = "server.example.com",
                Ip = "2001:db8::1",
            },
        },
        Id = 42,
        Ip = "131.232.99.1",
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels2",
            ["key1"] = "labels1",
        },
        Name = "my-resource",
        Protection = new Protection
        {
            Delete = false,
        },
        Type = Type50Enum.Ipv4,
    },
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
};
```



