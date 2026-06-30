# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByaWNlNg


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | `String` | Required | Name of the Location the price is for | String getLocation() | setLocation(String location) |
| `PriceMonthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location | PriceMonthly7 getPriceMonthly() | setPriceMonthly(PriceMonthly7 priceMonthly) |


# Example

```java
import cloud.hetzner.api.models.Price6;
import cloud.hetzner.api.models.PriceMonthly7;

Price6 price6 = new Price6.Builder(
    "fsn1",
    new PriceMonthly7.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .build()
)
.build();
```



