# Notifications

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5vdGlmaWNhdGlvbnM

The notification settings for a trigger alert.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Notifications`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Email` | `List<string>` | Required | An email to notify on an alert trigger. |
| `Slack` | [`List<Slack>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/slack.md) | Required | Slack integration details. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Notifications notifications = new Notifications
{
    Email = new List<string>
    {
        "bob@example.com",
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
};
```



