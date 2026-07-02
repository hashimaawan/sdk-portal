# V2 Images Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2ImagesActionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Type` | [`Type15`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-15.md) | Required | The action to be taken on the image. Can be either `convert` or `transfer`. | Type15 getType() | setType(Type15 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Type15;
import com.digitalocean.api.models.V2ImagesActionsRequest;
import java.io.IOException;

V2ImagesActionsRequest v2ImagesActionsRequest = new V2ImagesActionsRequest.Builder(
    Type15.CONVERT
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



