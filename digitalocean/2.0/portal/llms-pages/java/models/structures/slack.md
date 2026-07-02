# Slack

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNsYWNr

*This model accepts additional fields of type Object.*


# Class Name

`Slack`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Channel` | `String` | Required | Slack channel to notify of an alert trigger. | String getChannel() | setChannel(String channel) |
| `Url` | `String` | Required | Slack Webhook URL. | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Slack;
import java.io.IOException;

Slack slack = new Slack.Builder(
    "Production Alerts",
    "https://hooks.slack.com/services/T1234567/AAAAAAAA/ZZZZZZ"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



