# V2 Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistryRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` | String getName() | setName(String name) |
| `Region` | [`Region6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-6.md) | Optional | Slug of the region where registry data is stored. When not provided, a region will be selected. | Region6 getRegion() | setRegion(Region6 region) |
| `SubscriptionTierSlug` | [`SubscriptionTierSlug`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/subscription-tier-slug.md) | Required | The slug of the subscription tier to sign up for. Valid values can be retrieved using the options endpoint. | SubscriptionTierSlug getSubscriptionTierSlug() | setSubscriptionTierSlug(SubscriptionTierSlug subscriptionTierSlug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region6;
import com.digitalocean.api.models.SubscriptionTierSlug;
import com.digitalocean.api.models.V2RegistryRequest;
import java.io.IOException;

V2RegistryRequest v2RegistryRequest = new V2RegistryRequest.Builder(
    "example",
    SubscriptionTierSlug.BASIC
)
.region(Region6.FRA1)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



