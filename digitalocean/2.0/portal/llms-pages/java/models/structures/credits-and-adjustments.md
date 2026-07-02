# Credits and Adjustments

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWRpdHNBbmRBZGp1c3RtZW50cw

*This model accepts additional fields of type Object.*


# Class Name

`CreditsAndAdjustments`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Amount` | `String` | Optional | Total amount charged in USD | String getAmount() | setAmount(String amount) |
| `Name` | `String` | Optional | Name of the charge | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.CreditsAndAdjustments;
import java.io.IOException;

CreditsAndAdjustments creditsAndAdjustments = new CreditsAndAdjustments.Builder()
    .amount("3.45")
    .name("Overages")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



