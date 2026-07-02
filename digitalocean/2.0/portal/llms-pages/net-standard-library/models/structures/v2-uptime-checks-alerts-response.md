# V2 Uptime Checks Alerts Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2UptimeChecksAlertsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Alerts` | [`List<Alerts1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/alerts-1.md) | Optional | - |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2UptimeChecksAlertsResponse v2UptimeChecksAlertsResponse = new V2UptimeChecksAlertsResponse
{
    Meta = new Meta
    {
        Total = 1,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Alerts = new List<Alerts1>
    {
        new Alerts1
        {
            Id = new Guid("00000cea-0000-0000-0000-000000000000"),
            Comparison = Comparison.GreaterThan,
            Name = "name6",
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
            Period = Period.Enum10M,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Alerts1
        {
            Id = new Guid("00000cea-0000-0000-0000-000000000000"),
            Comparison = Comparison.GreaterThan,
            Name = "name6",
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
            Period = Period.Enum10M,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new Alerts1
        {
            Id = new Guid("00000cea-0000-0000-0000-000000000000"),
            Comparison = Comparison.GreaterThan,
            Name = "name6",
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
            Period = Period.Enum10M,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
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



