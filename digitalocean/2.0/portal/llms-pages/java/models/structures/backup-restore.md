# Backup Restore

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkJhY2t1cFJlc3RvcmU

*This model accepts additional fields of type Object.*


# Class Name

`BackupRestore`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BackupCreatedAt` | `LocalDateTime` | Optional | The timestamp of an existing database cluster backup in ISO8601 combined date and time format. The most recent backup will be used if excluded. | LocalDateTime getBackupCreatedAt() | setBackupCreatedAt(LocalDateTime backupCreatedAt) |
| `DatabaseName` | `String` | Required | The name of an existing database cluster from which the backup will be restored. | String getDatabaseName() | setDatabaseName(String databaseName) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.BackupRestore;
import java.io.IOException;

BackupRestore backupRestore = new BackupRestore.Builder(
    "backend"
)
.backupCreatedAt(DateTimeHelper.fromRfc8601DateTime("2019-01-31T19:25:22Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



