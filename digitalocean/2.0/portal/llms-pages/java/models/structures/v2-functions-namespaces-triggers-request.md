# V2 Functions Namespaces Triggers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2FunctionsNamespacesTriggersRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Function` | `String` | Required | Name of function(action) that exists in the given namespace. | String getFunction() | setFunction(String function) |
| `IsEnabled` | `boolean` | Required | Indicates weather the trigger is paused or unpaused. | boolean getIsEnabled() | setIsEnabled(boolean isEnabled) |
| `Name` | `String` | Required | The trigger's unique name within the namespace. | String getName() | setName(String name) |
| `ScheduledDetails` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/scheduled-details.md) | Required | Trigger details for SCHEDULED type, where body is optional. | ScheduledDetails getScheduledDetails() | setScheduledDetails(ScheduledDetails scheduledDetails) |
| `Type` | `String` | Required | One of different type of triggers. Currently only SCHEDULED is supported. | String getType() | setType(String type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Body;
import com.digitalocean.api.models.ScheduledDetails;
import com.digitalocean.api.models.V2FunctionsNamespacesTriggersRequest;
import java.io.IOException;

V2FunctionsNamespacesTriggersRequest v2FunctionsNamespacesTriggersRequest = new V2FunctionsNamespacesTriggersRequest.Builder(
    "hello",
    true,
    "my trigger",
    new ScheduledDetails.Builder(
        "* * * * *"
    )
    .body(new Body.Builder()
            .name("name6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    "SCHEDULED"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



