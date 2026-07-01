# Price per Tb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaWNlUGVyVGI

*This model accepts additional fields of type Object.*


# Class Name

`PricePerTb`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Gross` | `String` | Required | Price with VAT added | String getGross() | setGross(String gross) |
| `Net` | `String` | Required | Price without VAT | String getNet() | setNet(String net) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.PricePerTb;
import java.io.IOException;

PricePerTb pricePerTb = new PricePerTb.Builder(
    "1.1900000000000000",
    "1.0000000000"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



