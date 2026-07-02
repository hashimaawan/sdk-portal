# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkVycm9y

*This model accepts additional fields of type Object.*


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Code` | [`Code`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/code.md) | Optional | A code identifier that represents the failing condition.<br><br>Failing conditions:<br><br>- `incompatible_phase` - indicates that the deployment's phase is not suitable for rollback.<br>- `incompatible_result` - indicates that the deployment's result is not suitable for rollback.<br>- `exceeded_revision_limit` - indicates that the app has exceeded the rollback revision limits for its tier.<br>- `app_pinned` - indicates that there is already a rollback in progress and the app is pinned.<br>- `database_config_conflict` - indicates that the deployment's database config is different than the current config.<br>- `region_conflict` - indicates that the deployment's region differs from the current app region.<br><br>Warning conditions:<br><br>- `static_site_requires_rebuild` - indicates that the deployment contains at least one static site that will require a rebuild.<br>- `image_source_missing_digest` - indicates that the deployment contains at least one component with an image source that is missing a digest. | Code getCode() | setCode(Code code) |
| `Components` | `List<String>` | Optional | - | List<String> getComponents() | setComponents(List<String> components) |
| `Message` | `String` | Optional | A human-readable message describing the failing condition. | String getMessage() | setMessage(String message) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Code;
import com.digitalocean.api.models.Error;
import java.io.IOException;
import java.util.Arrays;

Error error = new Error.Builder()
    .code(Code.EXCEEDED_REVISION_LIMIT)
    .components(Arrays.asList(
        "www"
    ))
    .message("the deployment is past the maximum historical revision limit of 0 for the \"starter\" app tier")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



