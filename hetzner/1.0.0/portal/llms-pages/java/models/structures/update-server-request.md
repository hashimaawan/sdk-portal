# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | New name to set | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.UpdateServerRequest;
import java.io.IOException;

UpdateServerRequest updateServerRequest = new UpdateServerRequest.Builder()
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("my-server")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



