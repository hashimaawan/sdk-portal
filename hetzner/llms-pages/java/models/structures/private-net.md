# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ip` | `String` | Optional | - | String getIp() | setIp(String ip) |
| `Network` | `Integer` | Optional | - | Integer getNetwork() | setNetwork(Integer network) |


# Example

```java
import cloud.hetzner.api.models.PrivateNet;

PrivateNet privateNet = new PrivateNet.Builder()
    .ip("10.0.0.2")
    .network(4711)
    .build();
```



