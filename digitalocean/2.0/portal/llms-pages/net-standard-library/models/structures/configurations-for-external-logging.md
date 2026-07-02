# Configurations for External Logging

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25zJTI1MjBmb3IlMjUyMGV4dGVybmFsJTI1MjBsb2dnaW5nLg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`ConfigurationsForExternalLogging`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Datadog` | [`Datadog`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/datadog.md) | Optional | DataDog configuration. |
| `Logtail` | [`Logtail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/logtail.md) | Optional | Logtail configuration. |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `2`, *Maximum Length*: `42`, *Pattern*: `^[A-Za-z0-9()\[\]'"][-A-Za-z0-9_. \/()\[\]]{0,40}[A-Za-z0-9()\[\]'"]$` |
| `Papertrail` | [`Papertrail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/papertrail.md) | Optional | Papertrail configuration. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

ConfigurationsForExternalLogging configurationsForExternalLogging = new ConfigurationsForExternalLogging
{
    Name = "my_log_destination",
    Datadog = new Datadog
    {
        ApiKey = "api_key2",
        Endpoint = "endpoint8",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Logtail = new Logtail
    {
        Token = "token4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Papertrail = new Papertrail
    {
        Endpoint = "endpoint4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



