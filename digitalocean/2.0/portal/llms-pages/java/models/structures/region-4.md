# Region 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlZ2lvbjQ

*This model accepts additional fields of type Object.*


# Class Name

`Region4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | A DigitalOcean region where Kubernetes is available. | String getName() | setName(String name) |
| `Slug` | `String` | Optional | The identifier for a region for use when creating a new cluster. | String getSlug() | setSlug(String slug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region4;
import java.io.IOException;

Region4 region4 = new Region4.Builder()
    .name("New York 3")
    .slug("nyc3")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



