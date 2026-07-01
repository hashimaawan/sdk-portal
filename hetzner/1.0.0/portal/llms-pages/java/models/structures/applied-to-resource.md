# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server.md) | Optional | - | Server getServer() | setServer(Server server) |
| `Type` | [`Type5Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-5.md) | Optional | Type of resource referenced | Type5Enum getType() | setType(Type5Enum type) |


# Example

```java
import cloud.hetzner.api.models.AppliedToResource;
import cloud.hetzner.api.models.Server;
import cloud.hetzner.api.models.Type5Enum;

AppliedToResource appliedToResource = new AppliedToResource.Builder()
    .server(new Server.Builder(
        14
    )
    .build())
    .type(Type5Enum.SERVER)
    .build();
```



