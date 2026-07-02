# Notifications

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk5vdGlmaWNhdGlvbnM

The notification settings for a trigger alert.

*This model accepts additional fields of type Object.*


# Class Name

`Notifications`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Email` | `List<String>` | Required | An email to notify on an alert trigger. | List<String> getEmail() | setEmail(List<String> email) |
| `Slack` | [`List<Slack>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/slack.md) | Required | Slack integration details. | List<Slack> getSlack() | setSlack(List<Slack> slack) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Notifications;
import com.digitalocean.api.models.Slack;
import java.io.IOException;
import java.util.Arrays;

Notifications notifications = new Notifications.Builder(
    Arrays.asList(
        "bob@example.com"
    ),
    Arrays.asList(
        new Slack.Builder(
            "Production Alerts",
            "https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



