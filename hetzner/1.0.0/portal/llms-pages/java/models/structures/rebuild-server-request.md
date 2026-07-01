# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Image` | `String` | Required | ID or name of Image to rebuilt from. | String getImage() | setImage(String image) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.RebuildServerRequest;
import java.io.IOException;

RebuildServerRequest rebuildServerRequest = new RebuildServerRequest.Builder(
    "ubuntu-20.04"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



