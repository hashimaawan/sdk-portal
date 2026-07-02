# V2 Uptime Checks Alerts Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2UptimeChecksAlertsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Comparison` | [`Comparison`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/comparison.md) | Optional | The comparison operator used against the alert's threshold. | Comparison getComparison() | setComparison(Comparison comparison) |
| `Name` | `String` | Optional | A human-friendly display name. | String getName() | setName(String name) |
| `Notifications` | [`Notifications`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/notifications.md) | Optional | The notification settings for a trigger alert. | Notifications getNotifications() | setNotifications(Notifications notifications) |
| `Period` | [`Period`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/period.md) | Optional | Period of time the threshold must be exceeded to trigger the alert. | Period getPeriod() | setPeriod(Period period) |
| `Threshold` | `Integer` | Optional | The threshold at which the alert will enter a trigger state. The specific threshold is dependent on the alert type. | Integer getThreshold() | setThreshold(Integer threshold) |
| `Type` | [`Type20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-20.md) | Optional | The type of alert. | Type20 getType() | setType(Type20 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Comparison;
import com.digitalocean.api.models.Notifications;
import com.digitalocean.api.models.Period;
import com.digitalocean.api.models.Slack;
import com.digitalocean.api.models.Type20;
import com.digitalocean.api.models.V2UptimeChecksAlertsRequest;
import java.io.IOException;
import java.util.Arrays;

V2UptimeChecksAlertsRequest v2UptimeChecksAlertsRequest = new V2UptimeChecksAlertsRequest.Builder()
    .comparison(Comparison.GREATER_THAN)
    .name("Landing page degraded performance")
    .notifications(new Notifications.Builder(
        Arrays.asList(
            "email4",
            "email3"
        ),
        Arrays.asList(
            new Slack.Builder(
                "channel6",
                "url2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Slack.Builder(
                "channel6",
                "url2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Slack.Builder(
                "channel6",
                "url2"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        )
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
    .period(Period.ENUM_2M)
    .threshold(300)
    .type(Type20.LATENCY)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



