# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRk1ldGE


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/pagination.md) | Required | - | Pagination getPagination() | setPagination(Pagination pagination) |


# Example

```java
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;

Meta meta = new Meta.Builder(
    new Pagination.Builder(
        4D,
        4D,
        3D,
        25D,
        2D,
        100D
    )
    .build()
)
.build();
```



