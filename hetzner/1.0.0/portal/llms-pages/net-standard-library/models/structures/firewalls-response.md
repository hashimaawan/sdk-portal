# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewalls` | [`List<Firewall>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall.md) | Required | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

FirewallsResponse firewallsResponse = new FirewallsResponse
{
    Firewalls = new List<Firewall>
    {
        new Firewall
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
            },
            Created = "2016-01-30T23:55:00+00:00",
            Id = 42,
            Name = "my-resource",
            Rules = new List<Rule>
            {
                new Rule
                {
                    Direction = Direction.In,
                    Protocol = Protocol.Udp,
                    Description = "description2",
                    DestinationIps = new List<string>
                    {
                        "28.239.13.1/32",
                        "28.239.14.0/24",
                        "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                    },
                    Port = "80",
                    SourceIps = new List<string>
                    {
                        "28.239.13.1/32",
                        "28.239.14.0/24",
                        "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                    },
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Labels = new Dictionary<string, string>
            {
                ["key0"] = "labels4",
                ["key1"] = "labels5",
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



