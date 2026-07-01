# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RemoveFrom` | [`List<FirewallRemoveFromResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from | List<FirewallRemoveFromResources> getRemoveFrom() | setRemoveFrom(List<FirewallRemoveFromResources> removeFrom) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.FirewallRemoveFromResources;
import cloud.hetzner.api.models.LabelSelector5;
import cloud.hetzner.api.models.RemoveFromResourcesRequest;
import cloud.hetzner.api.models.Server9;
import cloud.hetzner.api.models.Type7;
import java.io.IOException;
import java.util.Arrays;

RemoveFromResourcesRequest removeFromResourcesRequest = new RemoveFromResourcesRequest.Builder(
    Arrays.asList(
        new FirewallRemoveFromResources.Builder()
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



