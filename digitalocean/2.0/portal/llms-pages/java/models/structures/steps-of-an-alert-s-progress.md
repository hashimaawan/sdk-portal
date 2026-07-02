# Steps of an Alert S Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlN0ZXBzJTI1MjBvZiUyNTIwYW4lMjUyMGFsZXJ0JTI1MjdzJTI1MjBwcm9ncmVzcy4

*This model accepts additional fields of type Object.*


# Class Name

`StepsOfAnAlertSProgress`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EndedAt` | `LocalDateTime` | Optional | - | LocalDateTime getEndedAt() | setEndedAt(LocalDateTime endedAt) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/reason.md) | Optional | - | Reason getReason() | setReason(Reason reason) |
| `StartedAt` | `LocalDateTime` | Optional | - | LocalDateTime getStartedAt() | setStartedAt(LocalDateTime startedAt) |
| `Status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-2.md) | Optional | **Default**: `Status2.UNKNOWN` | Status2 getStatus() | setStatus(Status2 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Reason;
import com.digitalocean.api.models.Status2;
import com.digitalocean.api.models.StepsOfAnAlertSProgress;
import java.io.IOException;

StepsOfAnAlertSProgress stepsOfAnAlertSProgress = new StepsOfAnAlertSProgress.Builder()
    .endedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-19T20:27:18Z"))
    .name("example_step")
    .reason(new Reason.Builder()
        .code("code2")
        .message("message4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .startedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-19T20:27:18Z"))
    .status(Status2.SUCCESS)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



