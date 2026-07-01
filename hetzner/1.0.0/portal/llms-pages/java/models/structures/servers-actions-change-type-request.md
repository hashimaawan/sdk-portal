# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ServerType` | `String` | Required | ID or name of Server type the Server should migrate to | String getServerType() | setServerType(String serverType) |
| `UpgradeDisk` | `boolean` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) | boolean getUpgradeDisk() | setUpgradeDisk(boolean upgradeDisk) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServersActionsChangeTypeRequest;
import java.io.IOException;

ServersActionsChangeTypeRequest serversActionsChangeTypeRequest = new ServersActionsChangeTypeRequest.Builder(
    "cx11",
    true
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



