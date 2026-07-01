# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Prices` | [`List<Price6>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-6.md) | Required | Floating IP type costs per Location | List<Price6> getPrices() | setPrices(List<Price6> prices) |
| `Type` | [`Type48Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-48.md) | Required | The type of the Floating IP | Type48Enum getType() | setType(Type48Enum type) |


# Example

```java
import cloud.hetzner.api.models.FloatingIp5;
import cloud.hetzner.api.models.Price6;
import cloud.hetzner.api.models.PriceMonthly7;
import cloud.hetzner.api.models.Type48Enum;
import java.util.Arrays;

FloatingIp5 floatingIp5 = new FloatingIp5.Builder(
    Arrays.asList(
        new Price6.Builder(
            "fsn1",
            new PriceMonthly7.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .build()
        )
        .build()
    ),
    Type48Enum.IPV4
)
.build();
```



