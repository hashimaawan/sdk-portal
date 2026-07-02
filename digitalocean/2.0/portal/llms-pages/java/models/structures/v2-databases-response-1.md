# V2 Databases Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Database` | [`Database1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/database-1.md) | Required | - | Database1 getDatabase() | setDatabase(Database1 database) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.Database1;
import com.digitalocean.api.models.Engine1;
import com.digitalocean.api.models.MaintenanceWindow;
import com.digitalocean.api.models.Status4;
import com.digitalocean.api.models.V2DatabasesResponse1;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2DatabasesResponse1 v2DatabasesResponse1 = new V2DatabasesResponse1.Builder(
    new Database1.Builder(
        Engine1.PG,
        "backend",
        2,
        "nyc3",
        "db-s-2vcpu-4gb"
    )
    .connection(new Connection.Builder()
            .database("database2")
            .host("host0")
            .password("password2")
            .port(174)
            .ssl(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2019-01-11T18:37:36Z"))
    .dbNames(Arrays.asList(
            "doadmin"
        ))
    .id(UUID.fromString("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"))
    .maintenanceWindow(new MaintenanceWindow.Builder(
            "day0",
            "hour8"
        )
        .description(Arrays.asList(
                "description3",
                "description2"
            ))
        .pending(false)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .privateNetworkUuid("d455e75d-4858-4eec-8c95-da2f0a5f93a7")
    .projectId(UUID.fromString("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"))
    .status(Status4.CREATING)
    .tags(Arrays.asList(
            "production"
        ))
    .version("10")
    .versionEndOfAvailability("2023-05-09T00:00:00Z")
    .versionEndOfLife("2023-11-09T00:00:00Z")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



