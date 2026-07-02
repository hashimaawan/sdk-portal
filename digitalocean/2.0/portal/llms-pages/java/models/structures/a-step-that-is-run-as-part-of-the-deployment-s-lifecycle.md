# A Step that Is Run as Part of the Deployment S Lifecycle

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkElMjUyMHN0ZXAlMjUyMHRoYXQlMjUyMGlzJTI1MjBydW4lMjUyMGFzJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhlJTI1MjBkZXBsb3ltZW50JTI1MjdzJTI1MjBsaWZlY3ljbGU

*This model accepts additional fields of type Object.*


# Class Name

`AStepThatIsRunAsPartOfTheDeploymentSLifecycle`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ComponentName` | `String` | Optional | - | String getComponentName() | setComponentName(String componentName) |
| `EndedAt` | `LocalDateTime` | Optional | - | LocalDateTime getEndedAt() | setEndedAt(LocalDateTime endedAt) |
| `MessageBase` | `String` | Optional | The base of a human-readable description of the step intended to be combined with the component name for presentation. For example:<br><br>`message_base` = "Building service"<br>`component_name` = "api" | String getMessageBase() | setMessageBase(String messageBase) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/reason.md) | Optional | - | Reason getReason() | setReason(Reason reason) |
| `StartedAt` | `LocalDateTime` | Optional | - | LocalDateTime getStartedAt() | setStartedAt(LocalDateTime startedAt) |
| `Status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-2.md) | Optional | **Default**: `Status2.UNKNOWN` | Status2 getStatus() | setStatus(Status2 status) |
| `Steps` | `List<Object>` | Optional | - | List<Object> getSteps() | setSteps(List<Object> steps) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle;
import com.digitalocean.api.models.Reason;
import com.digitalocean.api.models.Status2;
import java.io.IOException;

AStepThatIsRunAsPartOfTheDeploymentSLifecycle aStepThatIsRunAsPartOfTheDeploymentSLifecycle = new AStepThatIsRunAsPartOfTheDeploymentSLifecycle.Builder()
    .componentName("component")
    .endedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-19T20:27:18Z"))
    .messageBase("Building service")
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



