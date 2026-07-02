# V2 Apps Alerts Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsAlertsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Alerts` | [`List<Alert1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/alert-1.md) | Optional | - | List<Alert1> getAlerts() | setAlerts(List<Alert1> alerts) |
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
import com.digitalocean.api.models.V2AppsAlertsResponse;
import java.io.IOException;
import java.util.Arrays;

V2AppsAlertsResponse v2AppsAlertsResponse = new V2AppsAlertsResponse.Builder()
    .alerts(Arrays.asList(
        new Alert1.Builder()
            .componentName("component_name6")
            .emails(Arrays.asList(
                "emails5",
                "emails6"
            ))
            .id("id6")
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
            .build(),
        new Alert1.Builder()
            .componentName("component_name6")
            .emails(Arrays.asList(
                "emails5",
                "emails6"
            ))
            .id("id6")
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
            .build(),
        new Alert1.Builder()
            .componentName("component_name6")
            .emails(Arrays.asList(
                "emails5",
                "emails6"
            ))
            .id("id6")
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
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



