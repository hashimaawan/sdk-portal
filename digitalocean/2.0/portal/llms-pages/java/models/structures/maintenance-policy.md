# Maintenance Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk1haW50ZW5hbmNlUG9saWN5

An object specifying the maintenance window policy for the Kubernetes cluster.

*This model accepts additional fields of type Object.*


# Class Name

`MaintenancePolicy`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Day` | [`Day`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/day.md) | Optional | The day of the maintenance window policy. May be one of `monday` through `sunday`, or `any` to indicate an arbitrary week day. | Day getDay() | setDay(Day day) |
| `Duration` | `String` | Optional, Read-only | The duration of the maintenance window policy in human-readable format. | String getDuration() | setDuration(String duration) |
| `StartTime` | `String` | Optional | The start time in UTC of the maintenance window policy in 24-hour clock format / HH:MM notation (e.g., `15:00`). | String getStartTime() | setStartTime(String startTime) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Day;
import com.digitalocean.api.models.MaintenancePolicy;
import java.io.IOException;

MaintenancePolicy maintenancePolicy = new MaintenancePolicy.Builder()
    .day(Day.ANY)
    .duration("4h0m0s")
    .startTime("12:00")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



