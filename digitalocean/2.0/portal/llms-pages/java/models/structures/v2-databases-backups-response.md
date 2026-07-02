# V2 Databases Backups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEJhY2t1cHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesBackupsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Backups` | [`List<Backup>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/backup.md) | Required | - | List<Backup> getBackups() | setBackups(List<Backup> backups) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Backup;
import com.digitalocean.api.models.V2DatabasesBackupsResponse;
import java.io.IOException;
import java.util.Arrays;

V2DatabasesBackupsResponse v2DatabasesBackupsResponse = new V2DatabasesBackupsResponse.Builder(
    Arrays.asList(
        new Backup.Builder(
            DateTimeHelper.fromRfc8601DateTime("2019-01-31T19:25:22Z"),
            0.03364864D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



