# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRhcmdldA


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`List<HealthStatus>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/health-status.md) | Optional | - |
| `Server` | [`Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-11.md) | Optional | - |
| `Type` | `string` | Optional | - |
| `UsePrivateIp` | `bool?` | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

Target target = new Target
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
    Type = "server",
    UsePrivateIp = false,
};
```



