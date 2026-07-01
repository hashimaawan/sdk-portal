# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ

*This model accepts additional fields of type Object.*


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Ip` | `String` | Optional | - | String getIp() | setIp(String ip) |
| `Network` | `Integer` | Optional | - | Integer getNetwork() | setNetwork(Integer network) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.PrivateNet;
import java.io.IOException;

PrivateNet privateNet = new PrivateNet.Builder()
    .ip("10.0.0.2")
    .network(4711)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



