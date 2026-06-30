# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFwcGxpZWRUbw


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AppliedToResources` | [`List<AppliedToResource>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/applied-to-resource.md) | Optional | - | List<AppliedToResource> getAppliedToResources() | setAppliedToResources(List<AppliedToResource> appliedToResources) |
| `LabelSelector` | [`LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/label-selector.md) | Optional | - | LabelSelector getLabelSelector() | setLabelSelector(LabelSelector labelSelector) |
| `Server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/server.md) | Optional | - | Server getServer() | setServer(Server server) |
| `Type` | [`Type6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-6.md) | Required | Type of resource referenced | Type6Enum getType() | setType(Type6Enum type) |


# Example

```java
import cloud.hetzner.api.models.AppliedTo;
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.LabelSelector;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Type5Enum;
import cloud.hetzner.api.models.Type6Enum;
import java.util.Arrays;

AppliedTo appliedTo = new AppliedTo.Builder(
    Type6Enum.SERVER
)
.appliedToResources(Arrays.asList(
        new AppliedToResource.Builder()
            .server(new Server.Builder(
                14
            )
            .build())
            .type(Type5Enum.SERVER)
            .build(),
        new AppliedToResource.Builder()
            .server(new Server.Builder(
                14
            )
            .build())
            .type(Type5Enum.SERVER)
            .build()
    ))
.labelSelector(new LabelSelector.Builder(
        "selector8"
    )
    .build())
.server(new Server.Builder(
        14
    )
    .build())
.build();
```



