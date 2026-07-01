# Price

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNl

*This model accepts additional fields of type Object.*


# Class Name

`Price`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | `String` | Required | Name of the Location the price is for | String getLocation() | setLocation(String location) |
| `PriceHourly` | [`PriceHourly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-hourly.md) | Required | Hourly costs for a Resource in this Location | PriceHourly getPriceHourly() | setPriceHourly(PriceHourly priceHourly) |
| `PriceMonthly` | [`PriceMonthly`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-monthly.md) | Required | Monthly costs for a Resource in this Location | PriceMonthly getPriceMonthly() | setPriceMonthly(PriceMonthly priceMonthly) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Price;
import cloud.hetzner.api.models.PriceHourly;
import cloud.hetzner.api.models.PriceMonthly;
import java.io.IOException;

Price price = new Price.Builder(
    "fsn1",
    new PriceHourly.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new PriceMonthly.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



