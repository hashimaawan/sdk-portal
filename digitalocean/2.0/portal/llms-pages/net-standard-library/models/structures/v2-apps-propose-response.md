# V2 Apps Propose Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBQcm9wb3NlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2AppsProposeResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppCost` | `int?` | Optional | The monthly cost of the proposed app in USD using the next pricing plan tier. For example, if you propose an app that uses the Basic tier, the `app_tier_upgrade_cost` field displays the monthly cost of the app if it were to use the Professional tier. If the proposed app already uses the most expensive tier, the field is empty. |
| `AppIsStatic` | `bool?` | Optional | Indicates whether the app is a static app. |
| `AppNameAvailable` | `bool?` | Optional | Indicates whether the app name is available. |
| `AppNameSuggestion` | `string` | Optional | The suggested name if the proposed app name is unavailable. |
| `AppTierDowngradeCost` | `int?` | Optional | The monthly cost of the proposed app in USD using the previous pricing plan tier. For example, if you propose an app that uses the Professional tier, the `app_tier_downgrade_cost` field displays the monthly cost of the app if it were to use the Basic tier. If the proposed app already uses the lest expensive tier, the field is empty. |
| `ExistingStaticApps` | `string` | Optional | The maximum number of free static apps the account can have. We will charge you for any additional static apps. |
| `Spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/app-spec.md) | Optional | The desired configuration of an application. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2AppsProposeResponse v2AppsProposeResponse = new V2AppsProposeResponse
{
    AppCost = 5,
    AppIsStatic = true,
    AppNameAvailable = true,
    AppNameSuggestion = "newName",
    AppTierDowngradeCost = 17,
    ExistingStaticApps = "2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



