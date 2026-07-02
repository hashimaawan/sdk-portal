# V2 Registry Subscription Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwU3Vic2NyaXB0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistrySubscriptionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `TierSlug` | [`TierSlug`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/tier-slug.md) | Optional | The slug of the subscription tier to sign up for. | TierSlug getTierSlug() | setTierSlug(TierSlug tierSlug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.TierSlug;
import com.digitalocean.api.models.V2RegistrySubscriptionRequest;
import java.io.IOException;

V2RegistrySubscriptionRequest v2RegistrySubscriptionRequest = new V2RegistrySubscriptionRequest.Builder()
    .tierSlug(TierSlug.BASIC)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



