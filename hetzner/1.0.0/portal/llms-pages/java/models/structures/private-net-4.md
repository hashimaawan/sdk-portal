# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AliasIps` | `List<String>` | Optional | - | List<String> getAliasIps() | setAliasIps(List<String> aliasIps) |
| `Ip` | `String` | Optional | - | String getIp() | setIp(String ip) |
| `MacAddress` | `String` | Optional | - | String getMacAddress() | setMacAddress(String macAddress) |
| `Network` | `Integer` | Optional | - | Integer getNetwork() | setNetwork(Integer network) |


# Example

```java
import cloud.hetzner.api.models.PrivateNet4;
import java.util.Arrays;

PrivateNet4 privateNet4 = new PrivateNet4.Builder()
    .aliasIps(Arrays.asList(
        "alias_ips0",
        "alias_ips9"
    ))
    .ip("10.0.0.2")
    .macAddress("86:00:ff:2a:7d:e1")
    .network(4711)
    .build();
```



