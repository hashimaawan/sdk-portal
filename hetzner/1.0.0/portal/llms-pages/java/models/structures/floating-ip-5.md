# Floating Ip 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA1

*This model accepts additional fields of type Object.*


# Class Name

`FloatingIp5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Prices` | [`List<Price6>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-6.md) | Required | Floating IP type costs per Location | List<Price6> getPrices() | setPrices(List<Price6> prices) |
| `Type` | [`Type48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-48.md) | Required | The type of the Floating IP | Type48 getType() | setType(Type48 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.FloatingIp5;
import cloud.hetzner.api.models.Price6;
import cloud.hetzner.api.models.PriceMonthly7;
import cloud.hetzner.api.models.Type48;
import java.io.IOException;
import java.util.Arrays;

FloatingIp5 floatingIp5 = new FloatingIp5.Builder(
    Arrays.asList(
        new Price6.Builder(
            "fsn1",
            new PriceMonthly7.Builder(
                "1.1900000000000000",
                "1.0000000000"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ),
    Type48.IPV4
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



