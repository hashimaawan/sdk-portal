# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFwcGxpZWRUbw

*This model accepts additional fields of type Object.*


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AppliedToResources` | [`List<AppliedToResource>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/applied-to-resource.md) | Optional | - | List<AppliedToResource> getAppliedToResources() | setAppliedToResources(List<AppliedToResource> appliedToResources) |
| `LabelSelector` | [`LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/label-selector.md) | Optional | - | LabelSelector getLabelSelector() | setLabelSelector(LabelSelector labelSelector) |
| `Server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server.md) | Optional | - | Server getServer() | setServer(Server server) |
| `Type` | [`Type6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-6.md) | Required | Type of resource referenced | Type6 getType() | setType(Type6 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.AppliedTo;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.LabelSelector;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Type5;
import cloud.hetzner.api.models.Type6;
import java.io.IOException;
import java.util.Arrays;

AppliedTo appliedTo = new AppliedTo.Builder(
    Type6.SERVER
)
.appliedToResources(Arrays.asList(
        new AppliedToResource.Builder()
            .server(new Server.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .type(Type5.SERVER)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new AppliedToResource.Builder()
            .server(new Server.Builder(
                14
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .type(Type5.SERVER)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.labelSelector(new LabelSelector.Builder(
        "selector8"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.server(new Server.Builder(
        14
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



