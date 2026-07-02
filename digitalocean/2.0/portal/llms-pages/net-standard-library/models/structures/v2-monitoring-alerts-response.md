# V2 Monitoring Alerts Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2MonitoringAlertsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Policies` | [`List<Policy>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/policy.md) | Required | - |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2MonitoringAlertsResponse v2MonitoringAlertsResponse = new V2MonitoringAlertsResponse
{
    Policies = new List<Policy>
    {
        new Policy
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
            Uuid = "78b3da62-27e5-49ba-ac70-5db0b5935c64",
            MValue = 80,
            Window = Window1.Enum5M,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Meta = new Meta
    {
        Total = 1,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Links = new Links
    {
        Pages = LinksPages.FromPages(
            new Pages
            {
                Last = "last6",
                Next = "next2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            }
        ),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



