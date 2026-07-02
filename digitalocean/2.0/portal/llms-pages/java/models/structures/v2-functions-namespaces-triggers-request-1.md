# V2 Functions Namespaces Triggers Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type Object.*


# Class Name

`V2FunctionsNamespacesTriggersRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `IsEnabled` | `Boolean` | Optional | Indicates weather the trigger is paused or unpaused. | Boolean getIsEnabled() | setIsEnabled(Boolean isEnabled) |
| `ScheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. | ScheduledDetails getScheduledDetails() | setScheduledDetails(ScheduledDetails scheduledDetails) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Body;
import com.digitalocean.api.models.ScheduledDetails;
import com.digitalocean.api.models.V2FunctionsNamespacesTriggersRequest1;
import java.io.IOException;

V2FunctionsNamespacesTriggersRequest1 v2FunctionsNamespacesTriggersRequest1 = new V2FunctionsNamespacesTriggersRequest1.Builder()
    .isEnabled(true)
    .scheduledDetails(new ScheduledDetails.Builder(
        "cron2"
    )
    .body(new Body.Builder()
            .name("name6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



