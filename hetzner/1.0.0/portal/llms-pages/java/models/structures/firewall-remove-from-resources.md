# Firewall Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVtb3ZlRnJvbVJlc291cmNlcw

*This model accepts additional fields of type Object.*


# Class Name

`FirewallRemoveFromResources`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LabelSelector` | [`LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` | LabelSelector5 getLabelSelector() | setLabelSelector(LabelSelector5 labelSelector) |
| `Server` | [`Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` | Server9 getServer() | setServer(Server9 server) |
| `Type` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-7.md) | Optional | Type of the resource | Type7 getType() | setType(Type7 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.FirewallRemoveFromResources;
import cloud.hetzner.api.models.LabelSelector5;
import cloud.hetzner.api.models.Server9;
import cloud.hetzner.api.models.Type7;
import java.io.IOException;

FirewallRemoveFromResources firewallRemoveFromResources = new FirewallRemoveFromResources.Builder()
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
    .build();
```



