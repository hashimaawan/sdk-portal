# 1 Click

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRjFDbGljaw

*This model accepts additional fields of type Object.*


# Class Name

`M1Click`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Slug` | `String` | Required | The slug identifier for the 1-Click application. | String getSlug() | setSlug(String slug) |
| `Type` | `String` | Required | The type of the 1-Click application. | String getType() | setType(String type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.M1Click;
import java.io.IOException;

M1Click m1Click = new M1Click.Builder(
    "monitoring",
    "kubernetes"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



