# Load Balancer Type 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU2


# Class Name

`LoadBalancerType6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `double` | Required | ID of the Load Balancer type the price is for | double getId() | setId(double id) |
| `Name` | `String` | Required | Name of the Load Balancer type the price is for | String getName() | setName(String name) |
| `Prices` | [`List<Price7>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-7.md) | Required | Load Balancer type costs per Location | List<Price7> getPrices() | setPrices(List<Price7> prices) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancerType6;
import cloud.hetzner.api.models.Price7;
import cloud.hetzner.api.models.PriceHourly6;
import cloud.hetzner.api.models.PriceMonthly8;
import java.util.Arrays;

LoadBalancerType6 loadBalancerType6 = new LoadBalancerType6.Builder(
    1D,
    "lb11",
    Arrays.asList(
        new Price7.Builder(
            "fsn1",
            new PriceHourly6.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .build(),
            new PriceMonthly8.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .build()
        )
        .build()
    )
)
.build();
```



