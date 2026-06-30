# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ServerType` | `String` | Required | ID or name of Server type the Server should migrate to | String getServerType() | setServerType(String serverType) |
| `UpgradeDisk` | `boolean` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) | boolean getUpgradeDisk() | setUpgradeDisk(boolean upgradeDisk) |


# Example

```java
import cloud.hetzner.api.models.ServersActionsChangeTypeRequest;

ServersActionsChangeTypeRequest serversActionsChangeTypeRequest = new ServersActionsChangeTypeRequest.Builder(
    "cx11",
    true
)
.build();
```



