# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Rules` | [`List<Rule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

SetRulesRequest setRulesRequest = new SetRulesRequest
{
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
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



