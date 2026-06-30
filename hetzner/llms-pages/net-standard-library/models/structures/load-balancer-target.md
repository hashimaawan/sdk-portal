# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`List<HealthStatus>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/health-status.md) | Optional | List of health statuses of the services on this target |
| `Ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `LabelSelector` | [`LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets |
| `Server` | [`LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through |
| `Targets` | [`List<Target>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/target.md) | Optional | List of selected targets |
| `Type` | [`Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-29.md) | Required | Type of the resource |
| `UsePrivateIp` | `bool?` | Optional | Use the private network IP instead of the public IP. Default value is false. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

LoadBalancerTarget loadBalancerTarget = new LoadBalancerTarget
{
    Type = Type29Enum.LabelSelector,
    HealthStatus = new List<HealthStatus>
    {
        new HealthStatus
        {
            ListenPort = 142,
            Status = Status30Enum.Unknown,
        },
        new HealthStatus
        {
            ListenPort = 142,
            Status = Status30Enum.Unknown,
        },
    },
    Ip = new Ip
    {
        Ip = "ip8",
    },
    LabelSelector = new LabelSelector7
    {
        Selector = "selector8",
    },
    Server = new LoadBalancerTargetServer
    {
        Id = 14,
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
                    Status = Status30Enum.Unknown,
                },
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30Enum.Unknown,
                },
            },
            Server = new Server11
            {
                Id = 14,
            },
            Type = "type2",
            UsePrivateIp = false,
        },
        new Target
        {
            HealthStatus = new List<HealthStatus>
            {
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30Enum.Unknown,
                },
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30Enum.Unknown,
                },
            },
            Server = new Server11
            {
                Id = 14,
            },
            Type = "type2",
            UsePrivateIp = false,
        },
        new Target
        {
            HealthStatus = new List<HealthStatus>
            {
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30Enum.Unknown,
                },
                new HealthStatus
                {
                    ListenPort = 142,
                    Status = Status30Enum.Unknown,
                },
            },
            Server = new Server11
            {
                Id = 14,
            },
            Type = "type2",
            UsePrivateIp = false,
        },
    },
};
```



