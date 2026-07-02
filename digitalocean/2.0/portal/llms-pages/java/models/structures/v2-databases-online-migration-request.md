# V2 Databases Online Migration Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesOnlineMigrationRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DisableSsl` | `Boolean` | Optional | Enables SSL encryption when connecting to the source database. | Boolean getDisableSsl() | setDisableSsl(Boolean disableSsl) |
| `Source` | [`Source`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/source.md) | Optional | - | Source getSource() | setSource(Source source) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Source;
import com.digitalocean.api.models.V2DatabasesOnlineMigrationRequest;
import java.io.IOException;

V2DatabasesOnlineMigrationRequest v2DatabasesOnlineMigrationRequest = new V2DatabasesOnlineMigrationRequest.Builder()
    .disableSsl(false)
    .source(new Source.Builder()
        .database("database4")
        .host("host4")
        .password("password8")
        .port(180)
        .ssl(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



