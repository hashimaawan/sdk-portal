# V2 Databases Online Migration Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME9ubGluZSUyNTIwTWlncmF0aW9uJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesOnlineMigrationResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional | The time the migration was initiated, in ISO 8601 format. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Id` | `String` | Optional | The ID of the most recent migration. | String getId() | setId(String id) |
| `Status` | [`Status5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-5.md) | Optional | The current status of the migration. | Status5 getStatus() | setStatus(Status5 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Status5;
import com.digitalocean.api.models.V2DatabasesOnlineMigrationResponse;
import java.io.IOException;

V2DatabasesOnlineMigrationResponse v2DatabasesOnlineMigrationResponse = new V2DatabasesOnlineMigrationResponse.Builder()
    .createdAt("2020-10-29T15:57:38Z")
    .id("77b28fc8-19ff-11eb-8c9c-c68e24557488")
    .status(Status5.RUNNING)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



