# Alert 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFsZXJ0MQ

*This model accepts additional fields of type Object.*


# Class Name

`Alert1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ComponentName` | `String` | Optional | - | String getComponentName() | setComponentName(String componentName) |
| `Emails` | `List<String>` | Optional | - | List<String> getEmails() | setEmails(List<String> emails) |
| `Id` | `String` | Optional, Read-only | - | String getId() | setId(String id) |
| `Phase` | [`Phase1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/phase-1.md) | Optional | **Default**: `Phase1.UNKNOWN` | Phase1 getPhase() | setPhase(Phase1 phase) |
| `Progress` | [`Progress2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/progress-2.md) | Optional | - | Progress2 getProgress() | setProgress(Progress2 progress) |
| `SlackWebhooks` | [`List<SlackWebhooksToSendAlertsTo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - | List<SlackWebhooksToSendAlertsTo> getSlackWebhooks() | setSlackWebhooks(List<SlackWebhooksToSendAlertsTo> slackWebhooks) |
| `Spec` | [`Alert`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/alert.md) | Optional | - | Alert getSpec() | setSpec(Alert spec) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Alert1;
import com.digitalocean.api.models.Phase1;
import com.digitalocean.api.models.Progress2;
import com.digitalocean.api.models.Reason;
import com.digitalocean.api.models.Status2;
import com.digitalocean.api.models.StepsOfAnAlertSProgress;
import java.io.IOException;
import java.util.Arrays;

Alert1 alert1 = new Alert1.Builder()
    .componentName("backend")
    .emails(Arrays.asList(
        "sammy@digitalocean.com"
    ))
    .id("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf")
    .phase(Phase1.ACTIVE)
    .progress(new Progress2.Builder()
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
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



