# Next Backup Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk5leHRCYWNrdXBXaW5kb3c

The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start.

*This model accepts additional fields of type Object.*


# Class Name

`NextBackupWindow`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `End` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format specifying the end of the Droplet's backup window. | LocalDateTime getEnd() | setEnd(LocalDateTime end) |
| `Start` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format specifying the start of the Droplet's backup window. | LocalDateTime getStart() | setStart(LocalDateTime start) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.NextBackupWindow;
import java.io.IOException;

NextBackupWindow nextBackupWindow = new NextBackupWindow.Builder()
    .end(DateTimeHelper.fromRfc8601DateTime("2019-12-04T23:00:00Z"))
    .start(DateTimeHelper.fromRfc8601DateTime("2019-12-04T00:00:00Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



