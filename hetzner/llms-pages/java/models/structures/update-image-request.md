# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | New description of Image | String getDescription() | setDescription(String description) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Type` | [`Type24Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-24.md) | Optional | Destination Image type to convert to | Type24Enum getType() | setType(Type24Enum type) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Type24Enum;
import cloud.hetzner.api.models.UpdateImageRequest;
import java.io.IOException;

UpdateImageRequest updateImageRequest = new UpdateImageRequest.Builder()
    .description("My new Image description")
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .type(Type24Enum.SNAPSHOT)
    .build();
```



