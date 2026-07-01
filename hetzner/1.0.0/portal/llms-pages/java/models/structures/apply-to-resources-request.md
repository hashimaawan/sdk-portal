# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApplyTo` | [`List<FirewallApplyToResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to | List<FirewallApplyToResources> getApplyTo() | setApplyTo(List<FirewallApplyToResources> applyTo) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ApplyToResourcesRequest;
import cloud.hetzner.api.models.FirewallApplyToResources;
import cloud.hetzner.api.models.LabelSelector5;
import cloud.hetzner.api.models.Server9;
import cloud.hetzner.api.models.Type7;
import java.io.IOException;
import java.util.Arrays;

ApplyToResourcesRequest applyToResourcesRequest = new ApplyToResourcesRequest.Builder(
    Arrays.asList(
        new FirewallApplyToResources.Builder()
            .labelSelector(new LabelSelector5.Builder(
                "selector8"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .server(new Server9.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .type(Type7.SERVER)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



