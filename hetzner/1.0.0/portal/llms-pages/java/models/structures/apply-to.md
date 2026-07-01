# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFwcGx5VG8


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LabelSelector` | [`LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` | LabelSelector1 getLabelSelector() | setLabelSelector(LabelSelector1 labelSelector) |
| `Server` | [`Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` | Server2 getServer() | setServer(Server2 server) |
| `Type` | [`Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-7.md) | Required | Type of the resource | Type7Enum getType() | setType(Type7Enum type) |


# Example

```java
import cloud.hetzner.api.models.ApplyTo;
import cloud.hetzner.api.models.LabelSelector1;
import cloud.hetzner.api.models.Server2;
import cloud.hetzner.api.models.Type7Enum;

ApplyTo applyTo = new ApplyTo.Builder(
    Type7Enum.SERVER
)
.labelSelector(new LabelSelector1.Builder(
        "selector8"
    )
    .build())
.server(new Server2.Builder(
        14
    )
    .build())
.build();
```



