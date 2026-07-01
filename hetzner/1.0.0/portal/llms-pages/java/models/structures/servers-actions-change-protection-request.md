# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Delete` | `Boolean` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) | Boolean getDelete() | setDelete(Boolean delete) |
| `Rebuild` | `Boolean` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) | Boolean getRebuild() | setRebuild(Boolean rebuild) |


# Example

```java
import cloud.hetzner.api.models.ServersActionsChangeProtectionRequest;

ServersActionsChangeProtectionRequest serversActionsChangeProtectionRequest = new ServersActionsChangeProtectionRequest.Builder()
    .delete(true)
    .rebuild(true)
    .build();
```



