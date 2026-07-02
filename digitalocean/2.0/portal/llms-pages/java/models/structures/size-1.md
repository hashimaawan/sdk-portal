# Size 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNpemUx

*This model accepts additional fields of type Object.*


# Class Name

`Size1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | A Droplet size available for use in a Kubernetes node pool. | String getName() | setName(String name) |
| `Slug` | `String` | Optional | The identifier for a size for use when creating a new cluster. | String getSlug() | setSlug(String slug) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Size1;
import java.io.IOException;

Size1 size1 = new Size1.Builder()
    .name("s-1vcpu-2gb")
    .slug("s-1vcpu-2gb")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



