# V2 Tags Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNvdXJjZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2TagsResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Resources` | [`List<Resources3>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/resources-3.md) | Required | An array of objects containing resource_id and resource_type  attributes. | List<Resources3> getResources() | setResources(List<Resources3> resources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ResourceType2;
import com.digitalocean.api.models.Resources3;
import com.digitalocean.api.models.V2TagsResourcesRequest;
import java.io.IOException;
import java.util.Arrays;

V2TagsResourcesRequest v2TagsResourcesRequest = new V2TagsResourcesRequest.Builder(
    Arrays.asList(
        new Resources3.Builder()
            .resourceId("9569411")
            .resourceType(ResourceType2.DROPLET)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Resources3.Builder()
            .resourceId("7555620")
            .resourceType(ResourceType2.IMAGE)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Resources3.Builder()
            .resourceId("3d80cb72-342b-4aaa-b92e-4e4abb24a933")
            .resourceType(ResourceType2.VOLUME)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



