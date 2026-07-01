# Price 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlNw

*This model accepts additional fields of type Object.*


# Class Name

`Price7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | `String` | Required | Name of the Location the price is for | String getLocation() | setLocation(String location) |
| `PriceHourly` | [`PriceHourly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-hourly-6.md) | Required | Hourly costs for a Load Balancer type in this network zone | PriceHourly6 getPriceHourly() | setPriceHourly(PriceHourly6 priceHourly) |
| `PriceMonthly` | [`PriceMonthly8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-monthly-8.md) | Required | Monthly costs for a Load Balancer type in this network zone | PriceMonthly8 getPriceMonthly() | setPriceMonthly(PriceMonthly8 priceMonthly) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Price7;
import cloud.hetzner.api.models.PriceHourly6;
import cloud.hetzner.api.models.PriceMonthly8;
import java.io.IOException;

Price7 price7 = new Price7.Builder(
    "fsn1",
    new PriceHourly6.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    new PriceMonthly8.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



