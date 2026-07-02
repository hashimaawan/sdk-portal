# Databases

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFiYXNlcw

Tagged Resource Statistics include metadata regarding the resource type that has been tagged.

*This model accepts additional fields of type Object.*


# Class Name

`Databases`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Count` | `Integer` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` | Integer getCount() | setCount(Integer count) |
| `LastTaggedUri` | `String` | Optional | The URI for the last tagged object for this type of resource. | String getLastTaggedUri() | setLastTaggedUri(String lastTaggedUri) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Databases;
import java.io.IOException;

Databases databases = new Databases.Builder()
    .count(5)
    .lastTaggedUri("https://api.digitalocean.com/v2/images/7555620")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



