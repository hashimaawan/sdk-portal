# Actor

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkFjdG9y

*This model accepts additional fields of type Object.*


# Class Name

`Actor`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Account` | `String` | Optional | - | String getAccount() | setAccount(String account) |
| `Id` | `UUID` | Optional | - | UUID getId() | setId(UUID id) |
| `Jti` | `String` | Optional | - | String getJti() | setJti(String jti) |
| `RequestIp` | `String` | Optional | - | String getRequestIp() | setRequestIp(String requestIp) |
| `UserAgent` | `String` | Optional | - | String getUserAgent() | setUserAgent(String userAgent) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import java.util.UUID;
import local.m1password.ApiHelper;
import local.m1password.models.Actor;

Actor actor = new Actor.Builder()
    .account("account0")
    .id(UUID.fromString("0000193c-0000-0000-0000-000000000000"))
    .jti("jti2")
    .requestIp("requestIp4")
    .userAgent("userAgent6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



