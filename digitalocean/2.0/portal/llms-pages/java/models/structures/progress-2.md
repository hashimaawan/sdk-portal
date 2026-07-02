# Progress 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlByb2dyZXNzMg

*This model accepts additional fields of type Object.*


# Class Name

`Progress2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Steps` | [`List<StepsOfAnAlertSProgress>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/steps-of-an-alert-s-progress.md) | Optional | - | List<StepsOfAnAlertSProgress> getSteps() | setSteps(List<StepsOfAnAlertSProgress> steps) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Progress2;
import com.digitalocean.api.models.Reason;
import com.digitalocean.api.models.Status2;
import com.digitalocean.api.models.StepsOfAnAlertSProgress;
import java.io.IOException;
import java.util.Arrays;

Progress2 progress2 = new Progress2.Builder()
    .steps(Arrays.asList(
        new StepsOfAnAlertSProgress.Builder()
            .endedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .name("name2")
            .reason(new Reason.Builder()
                .code("code2")
                .message("message4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .startedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .status(Status2.SUCCESS)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new StepsOfAnAlertSProgress.Builder()
            .endedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .name("name2")
            .reason(new Reason.Builder()
                .code("code2")
                .message("message4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .startedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .status(Status2.SUCCESS)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



