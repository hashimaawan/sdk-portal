# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month

*This model accepts additional fields of type Object.*


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PricePerGbMonth` | [`PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-per-gb-month.md) | Required | - | PricePerGbMonth getPricePerGbMonth() | setPricePerGbMonth(PricePerGbMonth pricePerGbMonth) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Image3;
import cloud.hetzner.api.models.PricePerGbMonth;
import java.io.IOException;

Image3 image3 = new Image3.Builder(
    new PricePerGbMonth.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



