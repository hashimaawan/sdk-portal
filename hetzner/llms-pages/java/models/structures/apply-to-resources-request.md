# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ApplyTo` | [`List<FirewallApplyToResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to | List<FirewallApplyToResources> getApplyTo() | setApplyTo(List<FirewallApplyToResources> applyTo) |


# Example

```java
import cloud.hetzner.api.models.ApplyToResourcesRequest;
import cloud.hetzner.api.models.FirewallApplyToResources;
import cloud.hetzner.api.models.LabelSelector5;
import cloud.hetzner.api.models.Server9;
import cloud.hetzner.api.models.Type7Enum;
import java.util.Arrays;

ApplyToResourcesRequest applyToResourcesRequest = new ApplyToResourcesRequest.Builder(
    Arrays.asList(
        new FirewallApplyToResources.Builder()
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



