# Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkVycm9yMg

If issuance or renewal reports `failed`, this property contains information about what happened

*This model accepts additional fields of type Object.*


# Class Name

`Error2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `String` | Optional | - | String getCode() | setCode(String code) |
| `Message` | `String` | Optional | - | String getMessage() | setMessage(String message) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Error2;
import java.io.IOException;

Error2 error2 = new Error2.Builder()
    .code("code2")
    .message("message4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



