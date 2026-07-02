# V2 Databases Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Databases` | [`List<Database1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/database-1.md) | Optional | - | List<Database1> getDatabases() | setDatabases(List<Database1> databases) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.Database1;
import com.digitalocean.api.models.Engine1;
import com.digitalocean.api.models.MaintenanceWindow;
import com.digitalocean.api.models.V2DatabasesResponse;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2DatabasesResponse v2DatabasesResponse = new V2DatabasesResponse.Builder()
    .databases(Arrays.asList(
        new Database1.Builder(
            Engine1.REDIS,
            "name6",
            242,
            "region2",
            "size4"
        )
        .connection(new Connection.Builder()
                .database("database2")
                .host("host0")
                .password("password2")
                .port(174)
                .ssl(false)
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .createdAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .dbNames(Arrays.asList(
                "db_names7",
                "db_names8"
            ))
        .id(UUID.fromString("0000031c-0000-0000-0000-000000000000"))
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
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



