# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`UpdatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutoDelete` | `Boolean` | Optional | Delete this Primary IP when the resource it is assigned to is deleted | Boolean getAutoDelete() | setAutoDelete(Boolean autoDelete) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | New unique name to set | String getName() | setName(String name) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.UpdatePrimaryIpRequest;
import java.io.IOException;

UpdatePrimaryIpRequest updatePrimaryIpRequest = new UpdatePrimaryIpRequest.Builder()
    .autoDelete(true)
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("my-ip")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



