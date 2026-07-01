# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs

*This model accepts additional fields of type Object.*


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `Integer` | Optional | ID of the Resource | Integer getId() | setId(Integer id) |
| `Status` | [`Status72`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server | Status72 getStatus() | setStatus(Status72 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServerPublicNetFirewall;
import cloud.hetzner.api.models.Status72;
import java.io.IOException;

ServerPublicNetFirewall serverPublicNetFirewall = new ServerPublicNetFirewall.Builder()
    .id(42)
    .status(Status72.APPLIED)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



