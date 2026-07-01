# Price 9

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlOQ

*This model accepts additional fields of type Object.*


# Class Name

`Price9`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | `String` | Required | Name of the Location the price is for | String getLocation() | setLocation(String location) |
| `PriceHourly` | [`PriceHourly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-hourly-8.md) | Required | Hourly costs for a Server type in this Location | PriceHourly8 getPriceHourly() | setPriceHourly(PriceHourly8 priceHourly) |
| `PriceMonthly` | [`PriceMonthly10`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-monthly-10.md) | Required | Monthly costs for a Server type in this Location | PriceMonthly10 getPriceMonthly() | setPriceMonthly(PriceMonthly10 priceMonthly) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Price9;
import cloud.hetzner.api.models.PriceHourly8;
import cloud.hetzner.api.models.PriceMonthly10;
import java.io.IOException;

Price9 price9 = new Price9.Builder(
    "fsn1",
    new PriceHourly8.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new PriceMonthly10.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



