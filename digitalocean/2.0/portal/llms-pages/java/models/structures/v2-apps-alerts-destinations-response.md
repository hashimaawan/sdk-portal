# V2 Apps Alerts Destinations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsAlertsDestinationsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Alert` | [`Alert1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/alert-1.md) | Optional | - | Alert1 getAlert() | setAlert(Alert1 alert) |
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
import com.digitalocean.api.models.V2AppsAlertsDestinationsResponse;
import java.io.IOException;
import java.util.Arrays;

V2AppsAlertsDestinationsResponse v2AppsAlertsDestinationsResponse = new V2AppsAlertsDestinationsResponse.Builder()
    .alert(new Alert1.Builder()
        .componentName("component_name2")
        .emails(Arrays.asList(
            "emails9"
        ))
        .id("id0")
        .phase(Phase1.CONFIGURING)
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
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



