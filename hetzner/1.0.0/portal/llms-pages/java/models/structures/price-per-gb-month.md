# Price per Gb Month

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlUGVyR2JNb250aA


# Class Name

`PricePerGbMonth`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |


# Example

```java
import cloud.hetzner.api.models.PricePerGbMonth;

PricePerGbMonth pricePerGbMonth = new PricePerGbMonth.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.build();
```



