# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | New description of Image | String getDescription() | setDescription(String description) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Type` | [`Type24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/type-24.md) | Optional | Destination Image type to convert to | Type24 getType() | setType(Type24 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Type24;
import cloud.hetzner.api.models.UpdateImageRequest;
import java.io.IOException;

UpdateImageRequest updateImageRequest = new UpdateImageRequest.Builder()
    .description("My new Image description")
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .type(Type24.SNAPSHOT)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



