# V2 Images Actions Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type Object.*


# Class Name

`V2ImagesActionsRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-15.md) | Required | The action to be taken on the image. Can be either `convert` or `transfer`. | Type15 getType() | setType(Type15 type) |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. | Region2 getRegion() | setRegion(Region2 region) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.Type15;
import com.digitalocean.api.models.V2ImagesActionsRequest1;
import java.io.IOException;

V2ImagesActionsRequest1 v2ImagesActionsRequest1 = new V2ImagesActionsRequest1.Builder(
    Type15.CONVERT,
    Region2.NYC3
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



