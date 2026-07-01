# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`UpdatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutoDelete` | `Boolean` | Optional | Delete this Primary IP when the resource it is assigned to is deleted | Boolean getAutoDelete() | setAutoDelete(Boolean autoDelete) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | New unique name to set | String getName() | setName(String name) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.UpdatePrimaryIPRequest;
import java.io.IOException;

UpdatePrimaryIPRequest updatePrimaryIPRequest = new UpdatePrimaryIPRequest.Builder()
    .autoDelete(true)
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("my-ip")
    .build();
```



