# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Volume from being deleted | Boolean getDelete() | setDelete(Boolean delete) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.VolumesActionsChangeProtectionRequest;
import java.io.IOException;

VolumesActionsChangeProtectionRequest volumesActionsChangeProtectionRequest = new VolumesActionsChangeProtectionRequest.Builder()
    .delete(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



