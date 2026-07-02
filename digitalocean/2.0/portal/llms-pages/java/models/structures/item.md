# Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkl0ZW0

*This model accepts additional fields of type Object.*


# Class Name

`Item`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Amount` | `String` | Optional | Amount of the charge | String getAmount() | setAmount(String amount) |
| `Count` | `String` | Optional | Number of times the charge was applied | String getCount() | setCount(String count) |
| `Name` | `String` | Optional | Description of the charge | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Item;
import java.io.IOException;

Item item = new Item.Builder()
    .amount("10.00")
    .count("1")
    .name("Spaces Subscription")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



