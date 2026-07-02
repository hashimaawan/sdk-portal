# Resources 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc291cmNlczM

*This model accepts additional fields of type Object.*


# Class Name

`Resources3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResourceId` | `String` | Optional | The identifier of a resource. | String getResourceId() | setResourceId(String resourceId) |
| `ResourceType` | [`ResourceType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/resource-type-2.md) | Optional | The type of the resource. | ResourceType2 getResourceType() | setResourceType(ResourceType2 resourceType) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ResourceType2;
import com.digitalocean.api.models.Resources3;
import java.io.IOException;

Resources3 resources3 = new Resources3.Builder()
    .resourceId("3d80cb72-342b-4aaa-b92e-4e4abb24a933")
    .resourceType(ResourceType2.VOLUME)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



