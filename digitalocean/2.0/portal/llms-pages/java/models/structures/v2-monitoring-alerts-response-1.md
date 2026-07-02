# V2 Monitoring Alerts Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBBbGVydHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`V2MonitoringAlertsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Policy` | [`Policy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/policy.md) | Optional | - | Policy getPolicy() | setPolicy(Policy policy) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Alerts;
import com.digitalocean.api.models.Compare;
import com.digitalocean.api.models.Policy;
import com.digitalocean.api.models.Slack;
import com.digitalocean.api.models.Type17;
import com.digitalocean.api.models.V2MonitoringAlertsResponse1;
import com.digitalocean.api.models.Window1;
import java.io.IOException;
import java.util.Arrays;

V2MonitoringAlertsResponse1 v2MonitoringAlertsResponse1 = new V2MonitoringAlertsResponse1.Builder()
    .policy(new Policy.Builder(
        new Alerts.Builder(
            Arrays.asList(
                "email2",
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
        .build(),
        Compare.GREATERTHAN,
        "description4",
        false,
        Arrays.asList(
            "entities9"
        ),
        Arrays.asList(
            "tags9",
            "tags0",
            "tags1"
        ),
        Type17.ENUM_V1INSIGHTSDROPLETDISK_READ,
        "uuid0",
        149.36D,
        Window1.ENUM_30M
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



