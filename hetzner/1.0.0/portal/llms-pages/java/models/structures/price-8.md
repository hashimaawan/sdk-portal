# Price 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlOA


# Class Name

`Price8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | `String` | Required | Name of the Location the price is for | String getLocation() | setLocation(String location) |
| `PriceHourly` | [`PriceHourly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-hourly-7.md) | Required | Hourly costs for a Primary IP type in this Location | PriceHourly7 getPriceHourly() | setPriceHourly(PriceHourly7 priceHourly) |
| `PriceMonthly` | [`PriceMonthly9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-monthly-9.md) | Required | Monthly costs for a Primary IP type in this Location | PriceMonthly9 getPriceMonthly() | setPriceMonthly(PriceMonthly9 priceMonthly) |


# Example

```java
import cloud.hetzner.api.models.Price8;
import cloud.hetzner.api.models.PriceHourly7;
import cloud.hetzner.api.models.PriceMonthly9;

Price8 price8 = new Price8.Builder(
    "fsn1",
    new PriceHourly7.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build(),
    new PriceMonthly9.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build()
)
.build();
```



