# V2 Apps Alerts Destinations Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBBbGVydHMlMjUyMERlc3RpbmF0aW9ucyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsAlertsDestinationsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Emails` | `List<String>` | Optional | - | List<String> getEmails() | setEmails(List<String> emails) |
| `SlackWebhooks` | [`List<SlackWebhooksToSendAlertsTo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/slack-webhooks-to-send-alerts-to.md) | Optional | - | List<SlackWebhooksToSendAlertsTo> getSlackWebhooks() | setSlackWebhooks(List<SlackWebhooksToSendAlertsTo> slackWebhooks) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.SlackWebhooksToSendAlertsTo;
import com.digitalocean.api.models.V2AppsAlertsDestinationsRequest;
import java.io.IOException;
import java.util.Arrays;

V2AppsAlertsDestinationsRequest v2AppsAlertsDestinationsRequest = new V2AppsAlertsDestinationsRequest.Builder()
    .emails(Arrays.asList(
        "sammy@digitalocean.com"
    ))
    .slackWebhooks(Arrays.asList(
        new SlackWebhooksToSendAlertsTo.Builder()
            .channel("channel8")
            .url("url0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



