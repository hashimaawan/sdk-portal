# V2 Functions Namespaces Triggers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Function` | `string` | Required | Name of function(action) that exists in the given namespace. |
| `IsEnabled` | `bool` | Required | Indicates weather the trigger is paused or unpaused. |
| `Name` | `string` | Required | The trigger's unique name within the namespace. |
| `ScheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/scheduled-details.md) | Required | Trigger details for SCHEDULED type, where body is optional. |
| `Type` | `string` | Required | One of different type of triggers. Currently only SCHEDULED is supported. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2FunctionsNamespacesTriggersRequest v2FunctionsNamespacesTriggersRequest = new V2FunctionsNamespacesTriggersRequest
{
    Function = "hello",
    IsEnabled = true,
    Name = "my trigger",
    ScheduledDetails = new ScheduledDetails
    {
        Cron = "* * * * *",
        Body = new Body
        {
            Name = "name6",
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Type = "SCHEDULED",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



