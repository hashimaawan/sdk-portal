# V2 Apps Propose Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBQcm9wb3NlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsProposeResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appCost` | `?int` | Optional | The monthly cost of the proposed app in USD using the next pricing plan tier. For example, if you propose an app that uses the Basic tier, the `app_tier_upgrade_cost` field displays the monthly cost of the app if it were to use the Professional tier. If the proposed app already uses the most expensive tier, the field is empty. | getAppCost(): ?int | setAppCost(?int appCost): void |
| `appIsStatic` | `?bool` | Optional | Indicates whether the app is a static app. | getAppIsStatic(): ?bool | setAppIsStatic(?bool appIsStatic): void |
| `appNameAvailable` | `?bool` | Optional | Indicates whether the app name is available. | getAppNameAvailable(): ?bool | setAppNameAvailable(?bool appNameAvailable): void |
| `appNameSuggestion` | `?string` | Optional | The suggested name if the proposed app name is unavailable. | getAppNameSuggestion(): ?string | setAppNameSuggestion(?string appNameSuggestion): void |
| `appTierDowngradeCost` | `?int` | Optional | The monthly cost of the proposed app in USD using the previous pricing plan tier. For example, if you propose an app that uses the Professional tier, the `app_tier_downgrade_cost` field displays the monthly cost of the app if it were to use the Basic tier. If the proposed app already uses the lest expensive tier, the field is empty. | getAppTierDowngradeCost(): ?int | setAppTierDowngradeCost(?int appTierDowngradeCost): void |
| `existingStaticApps` | `?string` | Optional | The maximum number of free static apps the account can have. We will charge you for any additional static apps. | getExistingStaticApps(): ?string | setExistingStaticApps(?string existingStaticApps): void |
| `spec` | [`?AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/app-spec.md) | Optional | The desired configuration of an application. | getSpec(): ?AppSpec | setSpec(?AppSpec spec): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsProposeResponseBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsProposeResponse = V2AppsProposeResponseBuilder::init()
    ->appCost(5)
    ->appIsStatic(true)
    ->appNameAvailable(true)
    ->appNameSuggestion('newName')
    ->appTierDowngradeCost(17)
    ->existingStaticApps('2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



