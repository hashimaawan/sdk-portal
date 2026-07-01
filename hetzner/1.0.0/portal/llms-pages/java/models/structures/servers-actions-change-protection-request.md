# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) | Boolean getDelete() | setDelete(Boolean delete) |
| `Rebuild` | `Boolean` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) | Boolean getRebuild() | setRebuild(Boolean rebuild) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServersActionsChangeProtectionRequest;
import java.io.IOException;

ServersActionsChangeProtectionRequest serversActionsChangeProtectionRequest = new ServersActionsChangeProtectionRequest.Builder()
    .delete(true)
    .rebuild(true)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



