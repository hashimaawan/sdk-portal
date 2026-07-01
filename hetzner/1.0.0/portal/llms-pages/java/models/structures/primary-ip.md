# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaW1hcnlJcA


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Prices` | [`List<Price8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-8.md) | Required | Primary IP type costs per Location | List<Price8> getPrices() | setPrices(List<Price8> prices) |
| `Type` | [`Type49Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-49.md) | Required | The type of the Primary IP | Type49Enum getType() | setType(Type49Enum type) |


# Example

```java
import cloud.hetzner.api.models.Price8;
import cloud.hetzner.api.models.PriceHourly7;
import cloud.hetzner.api.models.PriceMonthly9;
import cloud.hetzner.api.models.PrimaryIp;
import cloud.hetzner.api.models.Type49Enum;
import java.util.Arrays;

PrimaryIp primaryIp = new PrimaryIp.Builder(
    Arrays.asList(
        new Price8.Builder(
            "fsn1",
            new PriceHourly7.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .build(),
            new PriceMonthly9.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .build()
        )
        .build()
    ),
    Type49Enum.IPV4
)
.build();
```



