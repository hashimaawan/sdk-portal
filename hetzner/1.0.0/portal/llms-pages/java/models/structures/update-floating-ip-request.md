# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`UpdateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Optional | New Description to set | String getDescription() | setDescription(String description) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Optional | New unique name to set | String getName() | setName(String name) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.UpdateFloatingIPRequest;
import java.io.IOException;

UpdateFloatingIPRequest updateFloatingIPRequest = new UpdateFloatingIPRequest.Builder()
    .description("Web Frontend")
    .labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
    .name("Web Frontend")
    .build();
```



