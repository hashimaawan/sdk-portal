# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type object.*


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppliedTo` | [`List<AppliedTo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/applied-to.md) | Required | - |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Id` | `int` | Required | ID of the Resource |
| `Labels` | `Dictionary<string, string>` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Rules` | [`List<Rule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/rule.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

Firewall firewall = new Firewall
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
        ["key0"] = "labels2",
        ["key1"] = "labels1",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



