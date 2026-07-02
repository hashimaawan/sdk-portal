# Scheduled Details

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNjaGVkdWxlZERldGFpbHM

Trigger details for SCHEDULED type, where body is optional.

*This model accepts additional fields of type Object.*


# Class Name

`ScheduledDetails`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Body` | [`Body`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/body.md) | Optional | Optional data to be sent to function while triggering the function. | Body getBody() | setBody(Body body) |
| `Cron` | `String` | Required | valid cron expression string which is required for SCHEDULED type triggers. | String getCron() | setCron(String cron) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Body;
import com.digitalocean.api.models.ScheduledDetails;
import java.io.IOException;

ScheduledDetails scheduledDetails = new ScheduledDetails.Builder(
    "* * * * *"
)
.body(new Body.Builder()
        .name("name6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



