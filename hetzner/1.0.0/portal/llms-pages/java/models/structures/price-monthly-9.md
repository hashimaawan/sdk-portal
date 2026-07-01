# Price Monthly 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlTW9udGhseTk

Monthly costs for a Primary IP type in this Location


# Class Name

`PriceMonthly9`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |


# Example

```java
import cloud.hetzner.api.models.PriceMonthly9;

PriceMonthly9 priceMonthly9 = new PriceMonthly9.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.build();
```



