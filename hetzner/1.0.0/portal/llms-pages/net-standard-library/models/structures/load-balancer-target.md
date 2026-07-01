# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA

*This model accepts additional fields of type object.*


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`List<HealthStatus>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/health-status.md) | Optional | List of health statuses of the services on this target |
| `Ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `LabelSelector` | [`LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets |
| `Server` | [`LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through |
| `Targets` | [`List<Target>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/target.md) | Optional | List of selected targets |
| `Type` | [`Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-29.md) | Required | Type of the resource |
| `UsePrivateIp` | `bool?` | Optional | Use the private network IP instead of the public IP. Default value is false. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

LoadBalancerTarget loadBalancerTarget = new LoadBalancerTarget
{
    Type = Type29.LabelSelector,
    HealthStatus = new List<HealthStatus>
    {
        new HealthStatus
        {
            ListenPort = 142,
            Status = Status30.Unknown,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new HealthStatus
        {
            ListenPort = 142,
            Status = Status30.Unknown,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Ip = new Ip
    {
        Ip = "ip8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    LabelSelector = new LabelSelector7
    {
        Selector = "selector8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Server = new LoadBalancerTargetServer
    {
        Id = 14,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Targets = new List<Target>
    {
        new Target
        {
            HealthStatus = new List<HealthStatus>
            {
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30.Unknown,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30.Unknown,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Server = new Server11
            {
                Id = 14,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Type = "type2",
            UsePrivateIp = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Target
        {
            HealthStatus = new List<HealthStatus>
            {
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30.Unknown,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30.Unknown,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Server = new Server11
            {
                Id = 14,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Type = "type2",
            UsePrivateIp = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Target
        {
            HealthStatus = new List<HealthStatus>
            {
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30.Unknown,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30.Unknown,
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Server = new Server11
            {
                Id = 14,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Type = "type2",
            UsePrivateIp = false,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



