# Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRyaWdnZXI

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Trigger`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `string` | Optional | UTC time string. |
| `Function` | `string` | Optional | Name of function(action) that exists in the given namespace. |
| `IsEnabled` | `bool?` | Optional | Indicates weather the trigger is paused or unpaused. |
| `Name` | `string` | Optional | The trigger's unique name within the namespace. |
| `Namespace` | `string` | Optional | A unique string format of UUID with a prefix fn-. |
| `ScheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `ScheduledRuns` | [`ScheduledRuns`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/scheduled-runs.md) | Optional | - |
| `Type` | `string` | Optional | String which indicates the type of trigger source like SCHEDULED. |
| `UpdatedAt` | `string` | Optional | UTC time string. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Trigger trigger = new Trigger
{
    CreatedAt = "2022-11-11T04:16:45Z",
    Function = "hello",
    IsEnabled = true,
    Name = "my trigger",
    MNamespace = "fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    Type = "SCHEDULED",
    UpdatedAt = "2022-11-11T04:16:45Z",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



