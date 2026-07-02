# V2 Uptime Checks Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwQWxlcnRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2UptimeChecksAlertsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Alert` | [`Alerts1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/alerts-1.md) | Optional | - | Alerts1 getAlert() | setAlert(Alerts1 alert) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Alerts1;
import com.digitalocean.api.models.Comparison;
import com.digitalocean.api.models.Notifications;
import com.digitalocean.api.models.Period;
import com.digitalocean.api.models.Slack;
import com.digitalocean.api.models.V2UptimeChecksAlertsResponse1;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2UptimeChecksAlertsResponse1 v2UptimeChecksAlertsResponse1 = new V2UptimeChecksAlertsResponse1.Builder()
    .alert(new Alerts1.Builder()
        .id(UUID.fromString("00002454-0000-0000-0000-000000000000"))
        .comparison(Comparison.GREATER_THAN)
        .name("name0")
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
        .period(Period.ENUM_30M)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



