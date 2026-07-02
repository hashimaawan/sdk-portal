# Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlRyaWdnZXI

*This model accepts additional fields of type Object.*


# Class Name

`Trigger`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional | UTC time string. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Function` | `String` | Optional | Name of function(action) that exists in the given namespace. | String getFunction() | setFunction(String function) |
| `IsEnabled` | `Boolean` | Optional | Indicates weather the trigger is paused or unpaused. | Boolean getIsEnabled() | setIsEnabled(Boolean isEnabled) |
| `Name` | `String` | Optional | The trigger's unique name within the namespace. | String getName() | setName(String name) |
| `Namespace` | `String` | Optional | A unique string format of UUID with a prefix fn-. | String getNamespace() | setNamespace(String namespace) |
| `ScheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. | ScheduledDetails getScheduledDetails() | setScheduledDetails(ScheduledDetails scheduledDetails) |
| `ScheduledRuns` | [`ScheduledRuns`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/scheduled-runs.md) | Optional | - | ScheduledRuns getScheduledRuns() | setScheduledRuns(ScheduledRuns scheduledRuns) |
| `Type` | `String` | Optional | String which indicates the type of trigger source like SCHEDULED. | String getType() | setType(String type) |
| `UpdatedAt` | `String` | Optional | UTC time string. | String getUpdatedAt() | setUpdatedAt(String updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Trigger;
import java.io.IOException;

Trigger trigger = new Trigger.Builder()
    .createdAt("2022-11-11T04:16:45Z")
    .function("hello")
    .isEnabled(true)
    .name("my trigger")
    .namespace("fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
    .type("SCHEDULED")
    .updatedAt("2022-11-11T04:16:45Z")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



