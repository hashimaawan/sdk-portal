# Health Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkhlYWx0aFN0YXR1cw

*This model accepts additional fields of type object.*


# Class Name

`HealthStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ListenPort` | `int?` | Optional | - |
| `Status` | [`Status30?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/status-30.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

HealthStatus healthStatus = new HealthStatus
{
    ListenPort = 443,
    Status = Status30.Healthy,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



