# Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkJhY2t1cA

*This model accepts additional fields of type Object.*


# Class Name

`Backup`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Required | A time value given in ISO8601 combined date and time format at which the backup was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `SizeGigabytes` | `double` | Required | The size of the database backup in GBs. | double getSizeGigabytes() | setSizeGigabytes(double sizeGigabytes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Backup;
import java.io.IOException;

Backup backup = new Backup.Builder(
    DateTimeHelper.fromRfc8601DateTime("2019-01-31T19:25:22Z"),
    0.03364864D
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



