# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AliasIps` | `List<String>` | Required | New alias IPs to set for this Server | List<String> getAliasIps() | setAliasIps(List<String> aliasIps) |
| `Network` | `int` | Required | ID of an existing Network already attached to the Server | int getNetwork() | setNetwork(int network) |


# Example

```java
import cloud.hetzner.api.models.ServersActionsChangeAliasIpsRequest;
import java.util.Arrays;

ServersActionsChangeAliasIpsRequest serversActionsChangeAliasIpsRequest = new ServersActionsChangeAliasIpsRequest.Builder(
    Arrays.asList(
        "10.0.1.2"
    ),
    4711
)
.build();
```



