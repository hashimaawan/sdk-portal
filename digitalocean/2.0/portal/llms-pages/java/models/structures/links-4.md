# Links 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxpbmtzNA

The links object contains the `self` object, which contains the resource relationship.

*This model accepts additional fields of type Object.*


# Class Name

`Links4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Self` | `String` | Optional | A URI that can be used to retrieve the resource. | String getSelf() | setSelf(String self) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Links4;
import java.io.IOException;

Links4 links4 = new Links4.Builder()
    .self("https://api.digitalocean.com/v2/droplets/13457723")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



