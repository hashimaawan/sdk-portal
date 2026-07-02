# V2 Monitoring Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alerts` | [`Alerts`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/alerts.md) | Required | - |
| `Compare` | [`Compare`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/compare.md) | Required | - |
| `Description` | `string` | Required | - |
| `Enabled` | `bool` | Required | - |
| `Entities` | `List<string>` | Required | - |
| `Tags` | `List<string>` | Required | - |
| `Type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-17.md) | Required | - |
| `MValue` | `double` | Required | - |
| `Window` | [`Window1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/window-1.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2MonitoringAlertsRequest v2MonitoringAlertsRequest = new V2MonitoringAlertsRequest
{
    Alerts = new Alerts
    {
        Email = new List<string>
        {
            "bob@exmaple.com",
        },
        Slack = new List<Slack>
        {
            new Slack
            {
                Channel = "Production Alerts",
                Url = "https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Compare = Compare.GreaterThan,
    Description = "CPU Alert",
    Enabled = true,
    Entities = new List<string>
    {
        "192018292",
    },
    Tags = new List<string>
    {
        "droplet_tag",
    },
    Type = Type17.EnumV1Insightsdropletcpu,
    MValue = 80,
    Window = Window1.Enum5M,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



