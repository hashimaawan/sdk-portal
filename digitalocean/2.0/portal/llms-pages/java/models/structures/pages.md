# Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBhZ2Vz

*This model accepts additional fields of type Object.*


# Class Name

`Pages`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Last` | `String` | Optional | URI of the last page of the results. | String getLast() | setLast(String last) |
| `Next` | `String` | Optional | URI of the next page of the results. | String getNext() | setNext(String next) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Pages;
import java.io.IOException;

Pages pages = new Pages.Builder()
    .last("https://api.digitalocean.com/v2/images?page=2")
    .next("https://api.digitalocean.com/v2/images?page=2")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



