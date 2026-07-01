# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PricePerTb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-per-tb.md) | Required | - | PricePerTb getPricePerTb() | setPricePerTb(PricePerTb pricePerTb) |


# Example

```java
import cloud.hetzner.api.models.PricePerTb;
import cloud.hetzner.api.models.Traffic;

Traffic traffic = new Traffic.Builder(
    new PricePerTb.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build()
)
.build();
```



