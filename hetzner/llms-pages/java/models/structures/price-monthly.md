# Price Monthly

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByaWNlTW9udGhseQ

Monthly costs for a Resource in this Location


# Class Name

`PriceMonthly`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |


# Example

```java
import cloud.hetzner.api.models.PriceMonthly;

PriceMonthly priceMonthly = new PriceMonthly.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.build();
```



