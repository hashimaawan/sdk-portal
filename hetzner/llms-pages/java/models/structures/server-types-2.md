# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg


# Class Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `double` | Required | ID of the Server type the price is for | double getId() | setId(double id) |
| `Name` | `String` | Required | Name of the Server type the price is for | String getName() | setName(String name) |
| `Prices` | [`List<Price9>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/price-9.md) | Required | Server type costs per Location | List<Price9> getPrices() | setPrices(List<Price9> prices) |


# Example

```java
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import cloud.hetzner.api.models.ServerTypes2;
import java.util.Arrays;

ServerTypes2 serverTypes2 = new ServerTypes2.Builder(
    4D,
    "cx11",
    Arrays.asList(
        new Price9.Builder(
            "fsn1",
            new PriceHourly8.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .build(),
            new PriceMonthly10.Builder(
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



