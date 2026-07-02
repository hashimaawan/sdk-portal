# Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlByb2dyZXNz

*This model accepts additional fields of type Object.*


# Class Name

`Progress`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ErrorSteps` | `Integer` | Optional | - | Integer getErrorSteps() | setErrorSteps(Integer errorSteps) |
| `PendingSteps` | `Integer` | Optional | - | Integer getPendingSteps() | setPendingSteps(Integer pendingSteps) |
| `RunningSteps` | `Integer` | Optional | - | Integer getRunningSteps() | setRunningSteps(Integer runningSteps) |
| `Steps` | [`List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - | List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle> getSteps() | setSteps(List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle> steps) |
| `SuccessSteps` | `Integer` | Optional | - | Integer getSuccessSteps() | setSuccessSteps(Integer successSteps) |
| `SummarySteps` | [`List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - | List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle> getSummarySteps() | setSummarySteps(List<AStepThatIsRunAsPartOfTheDeploymentSLifecycle> summarySteps) |
| `TotalSteps` | `Integer` | Optional | - | Integer getTotalSteps() | setTotalSteps(Integer totalSteps) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.AStepThatIsRunAsPartOfTheDeploymentSLifecycle;
import com.digitalocean.api.models.Progress;
import com.digitalocean.api.models.Reason;
import java.io.IOException;
import java.util.Arrays;

Progress progress = new Progress.Builder()
    .errorSteps(3)
    .pendingSteps(2)
    .runningSteps(2)
    .steps(Arrays.asList(
        new AStepThatIsRunAsPartOfTheDeploymentSLifecycle.Builder()
            .componentName("component_name0")
            .endedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .messageBase("message_base4")
            .name("name2")
            .reason(new Reason.Builder()
                .code("code2")
                .message("message4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new AStepThatIsRunAsPartOfTheDeploymentSLifecycle.Builder()
            .componentName("component_name0")
            .endedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .messageBase("message_base4")
            .name("name2")
            .reason(new Reason.Builder()
                .code("code2")
                .message("message4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new AStepThatIsRunAsPartOfTheDeploymentSLifecycle.Builder()
            .componentName("component_name0")
            .endedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .messageBase("message_base4")
            .name("name2")
            .reason(new Reason.Builder()
                .code("code2")
                .message("message4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .successSteps(4)
    .totalSteps(5)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



