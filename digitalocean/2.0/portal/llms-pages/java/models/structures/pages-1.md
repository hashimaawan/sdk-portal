# Pages 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBhZ2VzMQ

*This model accepts additional fields of type Object.*


# Class Name

`Pages1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `First` | `String` | Optional | URI of the first page of the results. | String getFirst() | setFirst(String first) |
| `Prev` | `String` | Optional | URI of the previous page of the results. | String getPrev() | setPrev(String prev) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Pages1;
import java.io.IOException;

Pages1 pages1 = new Pages1.Builder()
    .first("https://api.digitalocean.com/v2/images?page=1")
    .prev("https://api.digitalocean.com/v2/images?page=1")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



