# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null

*This model accepts additional fields of type Object.*


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | `String` | Required | Fixed machine readable code | String getCode() | setCode(String code) |
| `Message` | `String` | Required | Humanized error message | String getMessage() | setMessage(String message) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Error;
import java.io.IOException;

Error error = new Error.Builder(
    "action_failed",
    "Action failed"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



