# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action.md) | Optional | - |
| `Firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
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
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Started = "2016-01-30T23:55:00+00:00",
            Status = Status.Success,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Action
        {
            Command = "apply_firewall",
            Error = new Error
            {
                Code = "action_failed",
                Message = "Action failed",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new Resource
                {
                    Id = 38,
                    Type = "firewall",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Started = "2016-01-30T23:55:00+00:00",
            Status = Status.Success,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Firewall = new Firewall
    {
        AppliedTo = new List<AppliedTo>
        {
            new AppliedTo
            {
                Type = Type6.Server,
                AppliedToResources = new List<AppliedToResource>
                {
                    new AppliedToResource
                    {
                        Server = new Server
                        {
                            Id = 14,
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        Type = Type5.Server,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                LabelSelector = new LabelSelector
                {
                    Selector = "selector8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Server = new Server
                {
                    Id = 14,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new AppliedTo
            {
                Type = Type6.Server,
                AppliedToResources = new List<AppliedToResource>
                {
                    new AppliedToResource
                    {
                        Server = new Server
                        {
                            Id = 14,
                            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                        },
                        Type = Type5.Server,
                        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                    },
                },
                LabelSelector = new LabelSelector
                {
                    Selector = "selector8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                Server = new Server
                {
                    Id = 14,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Created = "created6",
        Id = 4,
        Name = "name6",
        Rules = new List<Rule>
        {
            new Rule
            {
                Direction = Direction.In,
                Protocol = Protocol.Udp,
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
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels2",
            ["key1"] = "labels1",
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



