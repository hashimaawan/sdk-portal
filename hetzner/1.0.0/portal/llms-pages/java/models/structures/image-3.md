# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-per-gb-month.md) | Required | - | PricePerGbMonth getPricePerGbMonth() | setPricePerGbMonth(PricePerGbMonth pricePerGbMonth) |


# Example

```java
import cloud.hetzner.api.models.Image3;
import cloud.hetzner.api.models.PricePerGbMonth;

Image3 image3 = new Image3.Builder(
    new PricePerGbMonth.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build()
)
.build();
```



