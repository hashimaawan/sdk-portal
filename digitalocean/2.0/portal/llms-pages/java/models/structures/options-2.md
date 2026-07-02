# Options 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk9wdGlvbnMy

*This model accepts additional fields of type Object.*


# Class Name

`Options2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AvailableRegions` | `List<String>` | Optional | - | List<String> getAvailableRegions() | setAvailableRegions(List<String> availableRegions) |
| `SubscriptionTiers` | [`List<SubscriptionTier>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/subscription-tier.md) | Optional | - | List<SubscriptionTier> getSubscriptionTiers() | setSubscriptionTiers(List<SubscriptionTier> subscriptionTiers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Options2;
import com.digitalocean.api.models.SubscriptionTier;
import java.io.IOException;
import java.util.Arrays;

Options2 options2 = new Options2.Builder()
    .availableRegions(Arrays.asList(
        "nyc3"
    ))
    .subscriptionTiers(Arrays.asList(
        new SubscriptionTier.Builder()
            .allowStorageOverage(false)
            .includedBandwidthBytes(172L)
            .includedRepositories(194)
            .includedStorageBytes(242L)
            .monthlyPriceInCents(236)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new SubscriptionTier.Builder()
            .allowStorageOverage(false)
            .includedBandwidthBytes(172L)
            .includedRepositories(194)
            .includedStorageBytes(242L)
            .monthlyPriceInCents(236)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new SubscriptionTier.Builder()
            .allowStorageOverage(false)
            .includedBandwidthBytes(172L)
            .includedRepositories(194)
            .includedStorageBytes(242L)
            .monthlyPriceInCents(236)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



