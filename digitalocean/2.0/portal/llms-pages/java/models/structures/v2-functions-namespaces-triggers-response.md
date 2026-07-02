# V2 Functions Namespaces Triggers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2FunctionsNamespacesTriggersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Triggers` | [`List<Trigger>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/trigger.md) | Optional | - | List<Trigger> getTriggers() | setTriggers(List<Trigger> triggers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Trigger;
import com.digitalocean.api.models.V2FunctionsNamespacesTriggersResponse;
import java.io.IOException;
import java.util.Arrays;

V2FunctionsNamespacesTriggersResponse v2FunctionsNamespacesTriggersResponse = new V2FunctionsNamespacesTriggersResponse.Builder()
    .triggers(Arrays.asList(
        new Trigger.Builder()
            .createdAt("created_at8")
            .function("function6")
            .isEnabled(false)
            .name("name0")
            .namespace("namespace2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



