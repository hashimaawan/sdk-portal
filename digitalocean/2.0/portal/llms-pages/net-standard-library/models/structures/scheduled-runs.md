# Scheduled Runs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNjaGVkdWxlZFJ1bnM

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ScheduledRuns`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LastRunAt` | `string` | Optional | Indicates last run time. null value indicates trigger not run yet. |
| `NextRunAt` | `string` | Optional | Indicates next run time. null value indicates trigger will not run. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

ScheduledRuns scheduledRuns = new ScheduledRuns
{
    LastRunAt = "2022-11-11T04:16:45Z",
    NextRunAt = "2022-11-11T04:16:45Z",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



