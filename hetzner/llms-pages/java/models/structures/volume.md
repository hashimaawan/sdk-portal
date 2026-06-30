# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlZvbHVtZQ

The cost of Volume per GB/month


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/price-per-gb-month.md) | Required | - | PricePerGbMonth getPricePerGbMonth() | setPricePerGbMonth(PricePerGbMonth pricePerGbMonth) |


# Example

```java
import cloud.hetzner.api.models.PricePerGbMonth;
import cloud.hetzner.api.models.Volume;

Volume volume = new Volume.Builder(
    new PricePerGbMonth.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build()
)
.build();
```



