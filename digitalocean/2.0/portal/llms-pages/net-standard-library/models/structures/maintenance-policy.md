# Maintenance Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlUG9saWN5

An object specifying the maintenance window policy for the Kubernetes cluster.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`MaintenancePolicy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Day` | [`Day?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/day.md) | Optional | The day of the maintenance window policy. May be one of `monday` through `sunday`, or `any` to indicate an arbitrary week day. |
| `Duration` | `string` | Optional, Read-only | The duration of the maintenance window policy in human-readable format. |
| `StartTime` | `string` | Optional | The start time in UTC of the maintenance window policy in 24-hour clock format / HH:MM notation (e.g., `15:00`). |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

MaintenancePolicy maintenancePolicy = new MaintenancePolicy
{
    Day = Day.Any,
    Duration = "4h0m0s",
    StartTime = "12:00",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



