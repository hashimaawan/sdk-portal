# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlOQ


# Class Name

`Price9`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | `String` | Required | Name of the Location the price is for | String getLocation() | setLocation(String location) |
| `PriceHourly` | [`PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location | PriceHourly8 getPriceHourly() | setPriceHourly(PriceHourly8 priceHourly) |
| `PriceMonthly` | [`PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location | PriceMonthly10 getPriceMonthly() | setPriceMonthly(PriceMonthly10 priceMonthly) |


# Example

```java
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;

Price9 price9 = new Price9.Builder(
    "fsn1",
    new PriceHourly8.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build(),
    new PriceMonthly10.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build()
)
.build();
```



