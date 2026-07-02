# V2 Functions Namespaces Triggers Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IsEnabled` | `bool?` | Optional | Indicates weather the trigger is paused or unpaused. |
| `ScheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2FunctionsNamespacesTriggersRequest1 v2FunctionsNamespacesTriggersRequest1 = new V2FunctionsNamespacesTriggersRequest1
{
    IsEnabled = true,
    ScheduledDetails = new ScheduledDetails
    {
        Cron = "cron2",
        Body = new Body
        {
            Name = "name6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



