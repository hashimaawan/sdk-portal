# Price Hourly 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlSG91cmx5OA

Hourly costs for a Server type in this Location


# Class Name

`PriceHourly8`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |


# Example

```java
import cloud.hetzner.api.models.PriceHourly8;

PriceHourly8 priceHourly8 = new PriceHourly8.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.build();
```



