# V2 Apps Rollback Validate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSb2xsYmFjayUyNTIwVmFsaWRhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsRollbackValidateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/error.md) | Optional | - | Error getError() | setError(Error error) |
| `Valid` | `Boolean` | Optional | Indicates whether the app can be rolled back to the specified deployment. | Boolean getValid() | setValid(Boolean valid) |
| `Warnings` | [`List<Warning>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/warning.md) | Optional | Contains a list of warnings that may cause the rollback to run under unideal circumstances. | List<Warning> getWarnings() | setWarnings(List<Warning> warnings) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Code;
import com.digitalocean.api.models.Error;
import com.digitalocean.api.models.V2AppsRollbackValidateResponse;
import com.digitalocean.api.models.Warning;
import java.io.IOException;
import java.util.Arrays;

V2AppsRollbackValidateResponse v2AppsRollbackValidateResponse = new V2AppsRollbackValidateResponse.Builder()
    .error(new Error.Builder()
        .code(Code.INCOMPATIBLE_PHASE)
        .components(Arrays.asList(
            "components3"
        ))
        .message("message4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .valid(false)
    .warnings(Arrays.asList(
        new Warning.Builder()
            .code(Code.EXCEEDED_REVISION_LIMIT)
            .components(Arrays.asList(
                "components3"
            ))
            .message("message4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Warning.Builder()
            .code(Code.EXCEEDED_REVISION_LIMIT)
            .components(Arrays.asList(
                "components3"
            ))
            .message("message4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



