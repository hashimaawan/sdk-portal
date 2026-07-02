# V2 Databases Maintenance Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME1haW50ZW5hbmNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesMaintenanceRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Day` | `String` | Required | The day of the week on which to apply maintenance updates. | String getDay() | setDay(String day) |
| `Description` | `List<String>` | Optional, Read-only | A list of strings, each containing information about a pending maintenance update. | List<String> getDescription() | setDescription(List<String> description) |
| `Hour` | `String` | Required | The hour in UTC at which maintenance updates will be applied in 24 hour format. | String getHour() | setHour(String hour) |
| `Pending` | `Boolean` | Optional, Read-only | A boolean value indicating whether any maintenance is scheduled to be performed in the next window. | Boolean getPending() | setPending(Boolean pending) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2DatabasesMaintenanceRequest;
import java.io.IOException;
import java.util.Arrays;

V2DatabasesMaintenanceRequest v2DatabasesMaintenanceRequest = new V2DatabasesMaintenanceRequest.Builder(
    "tuesday",
    "14:00"
)
.description(Arrays.asList(
        "Update TimescaleDB to version 1.2.1",
        "Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases"
    ))
.pending(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



