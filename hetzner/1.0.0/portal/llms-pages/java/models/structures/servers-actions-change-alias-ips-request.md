# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AliasIps` | `List<String>` | Required | New alias IPs to set for this Server | List<String> getAliasIps() | setAliasIps(List<String> aliasIps) |
| `Network` | `int` | Required | ID of an existing Network already attached to the Server | int getNetwork() | setNetwork(int network) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServersActionsChangeAliasIpsRequest;
import java.io.IOException;
import java.util.Arrays;

ServersActionsChangeAliasIpsRequest serversActionsChangeAliasIpsRequest = new ServersActionsChangeAliasIpsRequest.Builder(
    Arrays.asList(
        "10.0.1.2"
    ),
    4711
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



