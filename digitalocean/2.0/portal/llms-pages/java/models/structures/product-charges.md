# Product Charges

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlByb2R1Y3RDaGFyZ2Vz

*This model accepts additional fields of type Object.*


# Class Name

`ProductCharges`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Amount` | `String` | Optional | Total amount charged | String getAmount() | setAmount(String amount) |
| `Items` | [`List<Item>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/item.md) | Optional | List of amount, and grouped aggregates by resource type. | List<Item> getItems() | setItems(List<Item> items) |
| `Name` | `String` | Optional | Description of usage charges | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Item;
import com.digitalocean.api.models.ProductCharges;
import java.io.IOException;
import java.util.Arrays;

ProductCharges productCharges = new ProductCharges.Builder()
    .amount("12.34")
    .items(Arrays.asList(
        new Item.Builder()
            .amount("10.00")
            .count("1")
            .name("Spaces Subscription")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Item.Builder()
            .amount("2.34")
            .count("1")
            .name("Database Clusters")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .name("Product usage charges")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



