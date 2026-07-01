# Price 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlNg

*This model accepts additional fields of type Object.*


# Class Name

`Price6`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | `String` | Required | Name of the Location the price is for | String getLocation() | setLocation(String location) |
| `PriceMonthly` | [`PriceMonthly7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-monthly-7.md) | Required | Monthly costs for a Floating IP type in this Location | PriceMonthly7 getPriceMonthly() | setPriceMonthly(PriceMonthly7 priceMonthly) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Price6;
import cloud.hetzner.api.models.PriceMonthly7;
import java.io.IOException;

Price6 price6 = new Price6.Builder(
    "fsn1",
    new PriceMonthly7.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



