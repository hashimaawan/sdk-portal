# V2 Apps Metrics Bandwidth Daily Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsMetricsBandwidthDailyRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppIds` | `List<string>` | Required | A list of app IDs to query bandwidth metrics for.<br><br>**Constraints**: *Maximum Items*: `100` |
| `Date` | `DateTime?` | Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2AppsMetricsBandwidthDailyRequest v2AppsMetricsBandwidthDailyRequest = new V2AppsMetricsBandwidthDailyRequest
{
    AppIds = new List<string>
    {
        "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
        "c2a93513-8d9b-4223-9d61-5e7272c81cf5",
    },
    Date = DateTime.ParseExact("2023-01-17T00:00:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



