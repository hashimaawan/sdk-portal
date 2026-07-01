# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month

*This model accepts additional fields of type Object.*


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PriceMonthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/price-monthly-6.md) | Required | - | PriceMonthly6 getPriceMonthly() | setPriceMonthly(PriceMonthly6 priceMonthly) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.FloatingIp4;
import cloud.hetzner.api.models.PriceMonthly6;
import java.io.IOException;

FloatingIp4 floatingIp4 = new FloatingIp4.Builder(
    new PriceMonthly6.Builder(
        "1.1900000000000000",
        "1.0000000000"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



