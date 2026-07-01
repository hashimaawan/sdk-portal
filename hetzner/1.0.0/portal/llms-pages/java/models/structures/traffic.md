# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB

*This model accepts additional fields of type Object.*


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PricePerTb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-per-tb.md) | Required | - | PricePerTb getPricePerTb() | setPricePerTb(PricePerTb pricePerTb) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.PricePerTb;
import cloud.hetzner.api.models.Traffic;
import java.io.IOException;

Traffic traffic = new Traffic.Builder(
    new PricePerTb.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



