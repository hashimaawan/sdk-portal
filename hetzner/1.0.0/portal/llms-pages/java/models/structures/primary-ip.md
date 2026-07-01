# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaW1hcnlJcA

*This model accepts additional fields of type Object.*


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Prices` | [`List<Price8>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-8.md) | Required | Primary IP type costs per Location | List<Price8> getPrices() | setPrices(List<Price8> prices) |
| `Type` | [`Type49`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-49.md) | Required | The type of the Primary IP | Type49 getType() | setType(Type49 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Price8;
import cloud.hetzner.api.models.PriceHourly7;
import cloud.hetzner.api.models.PriceMonthly9;
import cloud.hetzner.api.models.PrimaryIp;
import cloud.hetzner.api.models.Type49;
import java.io.IOException;
import java.util.Arrays;

PrimaryIp primaryIp = new PrimaryIp.Builder(
    Arrays.asList(
        new Price8.Builder(
            "fsn1",
            new PriceHourly7.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new PriceMonthly9.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Type49.IPV4
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



