# Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVzcG9uc2U


# Class Name

`FirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewall` | [`Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

FirewallResponse firewallResponse = new FirewallResponse
{
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
        },
        Created = "2016-01-30T23:55:00+00:00",
        Id = 42,
        Name = "my-resource",
        Rules = new List<Rule>
        {
            new Rule
            {
                Direction = DirectionEnum.In,
                Protocol = ProtocolEnum.Udp,
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



