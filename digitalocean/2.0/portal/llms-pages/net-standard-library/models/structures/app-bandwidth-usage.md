# App Bandwidth Usage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcEJhbmR3aWR0aFVzYWdl

Bandwidth usage for an app.

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`AppBandwidthUsage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppId` | `string` | Optional | The ID of the app. |
| `BandwidthBytes` | `string` | Optional | The used bandwidth amount in bytes. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

AppBandwidthUsage appBandwidthUsage = new AppBandwidthUsage
{
    AppId = "4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf",
    BandwidthBytes = "513668",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



