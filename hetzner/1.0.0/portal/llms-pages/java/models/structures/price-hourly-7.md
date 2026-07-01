# Price Hourly 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlSG91cmx5Nw

Hourly costs for a Primary IP type in this Location


# Class Name

`PriceHourly7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |


# Example

```java
import cloud.hetzner.api.models.PriceHourly7;

PriceHourly7 priceHourly7 = new PriceHourly7.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.build();
```



