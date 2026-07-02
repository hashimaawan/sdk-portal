# V2 Registry Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwT3B0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistryOptionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Options` | [`Options2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/options-2.md) | Optional | - | Options2 getOptions() | setOptions(Options2 options) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Options2;
import com.digitalocean.api.models.SubscriptionTier;
import com.digitalocean.api.models.V2RegistryOptionsResponse;
import java.io.IOException;
import java.util.Arrays;

V2RegistryOptionsResponse v2RegistryOptionsResponse = new V2RegistryOptionsResponse.Builder()
    .options(new Options2.Builder()
        .availableRegions(Arrays.asList(
            "available_regions9"
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
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



