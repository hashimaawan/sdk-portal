# V2 Apps Propose Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBQcm9wb3NlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsProposeResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AppCost` | `Integer` | Optional | The monthly cost of the proposed app in USD using the next pricing plan tier. For example, if you propose an app that uses the Basic tier, the `app_tier_upgrade_cost` field displays the monthly cost of the app if it were to use the Professional tier. If the proposed app already uses the most expensive tier, the field is empty. | Integer getAppCost() | setAppCost(Integer appCost) |
| `AppIsStatic` | `Boolean` | Optional | Indicates whether the app is a static app. | Boolean getAppIsStatic() | setAppIsStatic(Boolean appIsStatic) |
| `AppNameAvailable` | `Boolean` | Optional | Indicates whether the app name is available. | Boolean getAppNameAvailable() | setAppNameAvailable(Boolean appNameAvailable) |
| `AppNameSuggestion` | `String` | Optional | The suggested name if the proposed app name is unavailable. | String getAppNameSuggestion() | setAppNameSuggestion(String appNameSuggestion) |
| `AppTierDowngradeCost` | `Integer` | Optional | The monthly cost of the proposed app in USD using the previous pricing plan tier. For example, if you propose an app that uses the Professional tier, the `app_tier_downgrade_cost` field displays the monthly cost of the app if it were to use the Basic tier. If the proposed app already uses the lest expensive tier, the field is empty. | Integer getAppTierDowngradeCost() | setAppTierDowngradeCost(Integer appTierDowngradeCost) |
| `ExistingStaticApps` | `String` | Optional | The maximum number of free static apps the account can have. We will charge you for any additional static apps. | String getExistingStaticApps() | setExistingStaticApps(String existingStaticApps) |
| `Spec` | [`AppSpec`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/app-spec.md) | Optional | The desired configuration of an application. | AppSpec getSpec() | setSpec(AppSpec spec) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2AppsProposeResponse;
import java.io.IOException;

V2AppsProposeResponse v2AppsProposeResponse = new V2AppsProposeResponse.Builder()
    .appCost(5)
    .appIsStatic(true)
    .appNameAvailable(true)
    .appNameSuggestion("newName")
    .appTierDowngradeCost(17)
    .existingStaticApps("2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



