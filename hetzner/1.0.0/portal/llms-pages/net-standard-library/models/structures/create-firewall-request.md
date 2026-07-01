# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplyTo` | [`List<ApplyTo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Firewall |
| `Rules` | [`List<Rule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/rule.md) | Optional | Array of rules |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Utilities;
using System.Collections.Generic;

CreateFirewallRequest createFirewallRequest = new CreateFirewallRequest
{
    Name = "Corporate Intranet Protection",
    ApplyTo = new List<ApplyTo>
    {
        new ApplyTo
        {
            Type = Type7Enum.Server,
            LabelSelector = new LabelSelector1
            {
                Selector = "selector8",
            },
            Server = new Server2
            {
                Id = 14,
            },
        },
        new ApplyTo
        {
            Type = Type7Enum.Server,
            LabelSelector = new LabelSelector1
            {
                Selector = "selector8",
            },
            Server = new Server2
            {
                Id = 14,
            },
        },
        new ApplyTo
        {
            Type = Type7Enum.Server,
            LabelSelector = new LabelSelector1
            {
                Selector = "selector8",
            },
            Server = new Server2
            {
                Id = 14,
            },
        },
    },
    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    Rules = new List<Rule>
    {
        new Rule
        {
            Direction = DirectionEnum.In,
            Protocol = ProtocolEnum.Tcp,
            Description = "description2",
            DestinationIps = new List<string>
            {
                "destination_ips1",
                "destination_ips2",
                "destination_ips3",
            },
            Port = "80",
            SourceIps = new List<string>
            {
                "28.239.13.1/32",
                "28.239.14.0/24",
                "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
            },
        },
    },
};
```



