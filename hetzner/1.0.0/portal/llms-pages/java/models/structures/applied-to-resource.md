# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl

*This model accepts additional fields of type Object.*


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server.md) | Optional | - | Server getServer() | setServer(Server server) |
| `Type` | [`Type5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-5.md) | Optional | Type of resource referenced | Type5 getType() | setType(Type5 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Type5;
import java.io.IOException;

AppliedToResource appliedToResource = new AppliedToResource.Builder()
    .server(new Server.Builder(
        14
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
    .type(Type5.SERVER)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



