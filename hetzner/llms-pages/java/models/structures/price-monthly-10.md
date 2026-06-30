# Price Monthly 10

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTEw

Monthly costs for a Server type in this Location


# Class Name

`PriceMonthly10`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |


# Example

```java
import cloud.hetzner.api.models.PriceMonthly10;

PriceMonthly10 priceMonthly10 = new PriceMonthly10.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.build();
```



