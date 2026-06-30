# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ListenPort` | `int?` | Optional | - |
| `Status` | [`Status30Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/status-30.md) | Optional | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

HealthStatus healthStatus = new HealthStatus
{
    ListenPort = 443,
    Status = Status30Enum.Healthy,
};
```



