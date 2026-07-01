# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`UpdateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | New Description to set | String getDescription() | setDescription(String description) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | New unique name to set | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.UpdateFloatingIpRequest;
import java.io.IOException;

UpdateFloatingIpRequest updateFloatingIpRequest = new UpdateFloatingIpRequest.Builder()
    .description("Web Frontend")
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("Web Frontend")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



