# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRhcmdldA

*This model accepts additional fields of type object.*


# Class Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `HealthStatus` | [`List<HealthStatus>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/health-status.md) | Optional | - |
| `Server` | [`Server11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server-11.md) | Optional | - |
| `Type` | `string` | Optional | - |
| `UsePrivateIp` | `bool?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

Target target = new Target
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
    Type = "server",
    UsePrivateIp = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



