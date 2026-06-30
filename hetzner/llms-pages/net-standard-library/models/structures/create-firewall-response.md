# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/action.md) | Optional | - |
| `Firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/firewall.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

CreateFirewallResponse createFirewallResponse = new CreateFirewallResponse
{
    Actions = new List<Action>
    {
        new Action
        {
            Command = "set_firewall_rules",
            Error = new Error
            {
                Code = "action_failed",
                Message = "Action failed",
            },
            Finished = "2016-01-30T23:56:00+00:00",
            Id = 13,
            Progress = 100,
            Resources = new List<Resource>
            {
                new Resource
                {
                    Id = 38,
                    Type = "firewall",
                },
            },
            Started = "2016-01-30T23:55:00+00:00",
            Status = StatusEnum.Success,
        },
        new Action
        {
            Command = "apply_firewall",
            Error = new Error
            {
                Code = "action_failed",
                Message = "Action failed",
            },
            Finished = "2016-01-30T23:56:00+00:00",
            Id = 14,
            Progress = 100,
            Resources = new List<Resource>
            {
                new Resource
                {
                    Id = 42,
                    Type = "server",
                },
                new Resource
                {
                    Id = 38,
                    Type = "firewall",
                },
            },
            Started = "2016-01-30T23:55:00+00:00",
            Status = StatusEnum.Success,
        },
    },
    Firewall = new Firewall
    {
        AppliedTo = new List<AppliedTo>
        {
            new AppliedTo
            {
                Type = Type6Enum.Server,
                AppliedToResources = new List<AppliedToResource>
                {
                    new AppliedToResource
                    {
                        Server = new Server
                        {
                            Id = 14,
                        },
                        Type = Type5Enum.Server,
                    },
                },
                LabelSelector = new LabelSelector
                {
                    Selector = "selector8",
                },
                Server = new Server
                {
                    Id = 14,
                },
            },
            new AppliedTo
            {
                Type = Type6Enum.Server,
                AppliedToResources = new List<AppliedToResource>
                {
                    new AppliedToResource
                    {
                        Server = new Server
                        {
                            Id = 14,
                        },
                        Type = Type5Enum.Server,
                    },
                },
                LabelSelector = new LabelSelector
                {
                    Selector = "selector8",
                },
                Server = new Server
                {
                    Id = 14,
                },
            },
        },
        Created = "created6",
        Id = 4,
        Name = "name6",
        Rules = new List<Rule>
        {
            new Rule
            {
                Direction = DirectionEnum.In,
                Protocol = ProtocolEnum.Udp,
                Description = "description2",
                DestinationIps = new List<string>
                {
                    "destination_ips1",
                    "destination_ips2",
                    "destination_ips3",
                },
                Port = "port8",
                SourceIps = new List<string>
                {
                    "source_ips1",
                    "source_ips2",
                    "source_ips3",
                },
            },
        },
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels2",
            ["key1"] = "labels1",
        },
    },
};
```



