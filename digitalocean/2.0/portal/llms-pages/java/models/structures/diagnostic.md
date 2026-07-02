# Diagnostic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRpYWdub3N0aWM

*This model accepts additional fields of type Object.*


# Class Name

`Diagnostic`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CheckName` | `String` | Optional | The clusterlint check that resulted in the diagnostic. | String getCheckName() | setCheckName(String checkName) |
| `Message` | `String` | Optional | Feedback about the object for users to fix. | String getMessage() | setMessage(String message) |
| `Object` | [`ObjectType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/object-type.md) | Optional | Metadata about the Kubernetes API object the diagnostic is reported on. | ObjectType getObject() | setObject(ObjectType object) |
| `Severity` | `String` | Optional | Can be one of error, warning or suggestion. | String getSeverity() | setSeverity(String severity) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Diagnostic;
import com.digitalocean.api.models.ObjectType;
import java.io.IOException;

Diagnostic diagnostic = new Diagnostic.Builder()
    .checkName("unused-config-map")
    .message("Unused config map")
    .object(new ObjectType.Builder()
        .kind("kind0")
        .name("name2")
        .namespace("namespace0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .severity("warning")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



