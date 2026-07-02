# V2 Functions Namespaces Triggers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2FunctionsNamespacesTriggersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Trigger` | [`Trigger`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/trigger.md) | Optional | - | Trigger getTrigger() | setTrigger(Trigger trigger) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Trigger;
import com.digitalocean.api.models.V2FunctionsNamespacesTriggersResponse1;
import java.io.IOException;

V2FunctionsNamespacesTriggersResponse1 v2FunctionsNamespacesTriggersResponse1 = new V2FunctionsNamespacesTriggersResponse1.Builder()
    .trigger(new Trigger.Builder()
        .createdAt("created_at6")
        .function("function6")
        .isEnabled(false)
        .name("name8")
        .namespace("namespace4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



