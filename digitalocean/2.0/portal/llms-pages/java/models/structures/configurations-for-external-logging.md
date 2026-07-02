# Configurations for External Logging

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25zJTI1MjBmb3IlMjUyMGV4dGVybmFsJTI1MjBsb2dnaW5nLg

*This model accepts additional fields of type Object.*


# Class Name

`ConfigurationsForExternalLogging`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Datadog` | [`Datadog`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/datadog.md) | Optional | DataDog configuration. | Datadog getDatadog() | setDatadog(Datadog datadog) |
| `Logtail` | [`Logtail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/logtail.md) | Optional | Logtail configuration. | Logtail getLogtail() | setLogtail(Logtail logtail) |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `2`, *Maximum Length*: `42`, *Pattern*: `^[A-Za-z0-9()\[\]'"][-A-Za-z0-9_. \/()\[\]]{0,40}[A-Za-z0-9()\[\]'"]$` | String getName() | setName(String name) |
| `Papertrail` | [`Papertrail`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/papertrail.md) | Optional | Papertrail configuration. | Papertrail getPapertrail() | setPapertrail(Papertrail papertrail) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.ConfigurationsForExternalLogging;
import com.digitalocean.api.models.Datadog;
import com.digitalocean.api.models.Logtail;
import com.digitalocean.api.models.Papertrail;
import java.io.IOException;

ConfigurationsForExternalLogging configurationsForExternalLogging = new ConfigurationsForExternalLogging.Builder(
    "my_log_destination"
)
.datadog(new Datadog.Builder(
        "api_key2"
    )
    .endpoint("endpoint8")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.logtail(new Logtail.Builder()
        .token("token4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.papertrail(new Papertrail.Builder(
        "endpoint4"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



