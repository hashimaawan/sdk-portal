# Sticky Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlN0aWNreVNlc3Npb25z

An object specifying sticky sessions settings for the load balancer.

*This model accepts additional fields of type Object.*


# Class Name

`StickySessions`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CookieName` | `String` | Optional | The name of the cookie sent to the client. This attribute is only returned when using `cookies` for the sticky sessions type. | String getCookieName() | setCookieName(String cookieName) |
| `CookieTtlSeconds` | `Integer` | Optional | The number of seconds until the cookie set by the load balancer expires. This attribute is only returned when using `cookies` for the sticky sessions type. | Integer getCookieTtlSeconds() | setCookieTtlSeconds(Integer cookieTtlSeconds) |
| `Type` | [`Type16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-16.md) | Optional | An attribute indicating how and if requests from a client will be persistently served by the same backend Droplet. The possible values are `cookies` or `none`.<br><br>**Default**: `Type16.NONE` | Type16 getType() | setType(Type16 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.StickySessions;
import com.digitalocean.api.models.Type16;
import java.io.IOException;

StickySessions stickySessions = new StickySessions.Builder()
    .cookieName("DO-LB")
    .cookieTtlSeconds(300)
    .type(Type16.COOKIES)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



