# Price Monthly 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTY


# Class Name

`PriceMonthly6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |


# Example

```java
import cloud.hetzner.api.models.PriceMonthly6;

PriceMonthly6 priceMonthly6 = new PriceMonthly6.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.build();
```



