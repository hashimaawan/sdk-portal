# V2 Uptime Checks Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Comparison` | [`Comparison?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/comparison.md) | Optional | The comparison operator used against the alert's threshold. |
| `Name` | `string` | Optional | A human-friendly display name. |
| `Notifications` | [`Notifications`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/notifications.md) | Optional | The notification settings for a trigger alert. |
| `Period` | [`Period?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/period.md) | Optional | Period of time the threshold must be exceeded to trigger the alert. |
| `Threshold` | `int?` | Optional | The threshold at which the alert will enter a trigger state. The specific threshold is dependent on the alert type. |
| `Type` | [`Type20?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-20.md) | Optional | The type of alert. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2UptimeChecksAlertsRequest v2UptimeChecksAlertsRequest = new V2UptimeChecksAlertsRequest
{
    Comparison = Comparison.GreaterThan,
    Name = "Landing page degraded performance",
    Notifications = new Notifications
    {
        Email = new List<string>
        {
            "email4",
            "email3",
        },
        Slack = new List<Slack>
        {
            new Slack
            {
                Channel = "channel6",
                Url = "url2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Slack
            {
                Channel = "channel6",
                Url = "url2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Slack
            {
                Channel = "channel6",
                Url = "url2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Period = Period.Enum2M,
    Threshold = 300,
    Type = Type20.Latency,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



