# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `RemoveFrom` | [`List<FirewallRemoveFromResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from | List<FirewallRemoveFromResources> getRemoveFrom() | setRemoveFrom(List<FirewallRemoveFromResources> removeFrom) |


# Example

```java
import cloud.hetzner.api.models.FirewallRemoveFromResources;
import cloud.hetzner.api.models.LabelSelector5;
import cloud.hetzner.api.models.RemoveFromResourcesRequest;
import cloud.hetzner.api.models.Server9;
import cloud.hetzner.api.models.Type7Enum;
import java.util.Arrays;

RemoveFromResourcesRequest removeFromResourcesRequest = new RemoveFromResourcesRequest.Builder(
    Arrays.asList(
        new FirewallRemoveFromResources.Builder()
            .labelSelector(new LabelSelector5.Builder(
                "selector8"
            )
            .build())
            .server(new Server9.Builder(
                14
            )
            .build())
            .type(Type7Enum.SERVER)
            .build()
    )
)
.build();
```



