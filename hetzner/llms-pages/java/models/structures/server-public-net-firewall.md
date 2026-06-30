# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `Integer` | Optional | ID of the Resource | Integer getId() | setId(Integer id) |
| `Status` | [`Status72Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server | Status72Enum getStatus() | setStatus(Status72Enum status) |


# Example

```java
import cloud.hetzner.api.models.ServerPublicNetFirewall;
import cloud.hetzner.api.models.Status72Enum;

ServerPublicNetFirewall serverPublicNetFirewall = new ServerPublicNetFirewall.Builder()
    .id(42)
    .status(Status72Enum.APPLIED)
    .build();
```



