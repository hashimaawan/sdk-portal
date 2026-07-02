# Cors

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNvcnM

*This model accepts additional fields of type Object.*


# Class Name

`Cors`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AllowCredentials` | `Boolean` | Optional | Whether browsers should expose the response to the client-side JavaScript code when the request’s credentials mode is include. This configures the `Access-Control-Allow-Credentials` header. | Boolean getAllowCredentials() | setAllowCredentials(Boolean allowCredentials) |
| `AllowHeaders` | `List<String>` | Optional | The set of allowed HTTP request headers. This configures the `Access-Control-Allow-Headers` header. | List<String> getAllowHeaders() | setAllowHeaders(List<String> allowHeaders) |
| `AllowMethods` | `List<String>` | Optional | The set of allowed HTTP methods. This configures the `Access-Control-Allow-Methods` header. | List<String> getAllowMethods() | setAllowMethods(List<String> allowMethods) |
| `AllowOrigins` | [`List<AllowOrigin>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/allow-origin.md) | Optional | The set of allowed CORS origins. | List<AllowOrigin> getAllowOrigins() | setAllowOrigins(List<AllowOrigin> allowOrigins) |
| `ExposeHeaders` | `List<String>` | Optional | The set of HTTP response headers that browsers are allowed to access. This configures the `Access-Control-Expose-Headers` header. | List<String> getExposeHeaders() | setExposeHeaders(List<String> exposeHeaders) |
| `MaxAge` | `String` | Optional | An optional duration specifying how long browsers can cache the results of a preflight request. This configures the `Access-Control-Max-Age` header. | String getMaxAge() | setMaxAge(String maxAge) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AllowOrigin;
import com.digitalocean.api.models.Cors;
import java.io.IOException;
import java.util.Arrays;

Cors cors = new Cors.Builder()
    .allowCredentials(false)
    .allowHeaders(Arrays.asList(
        "Content-Type",
        "X-Custom-Header"
    ))
    .allowMethods(Arrays.asList(
        "GET",
        "OPTIONS",
        "POST",
        "PUT",
        "PATCH",
        "DELETE"
    ))
    .allowOrigins(Arrays.asList(
        new AllowOrigin.Builder()
            .exact("https://www.example.com")
            .prefix("prefix6")
            .regex("regex4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new AllowOrigin.Builder()
            .exact("exact8")
            .prefix("prefix6")
            .regex("^.*example.com")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .exposeHeaders(Arrays.asList(
        "Content-Encoding",
        "X-Custom-Header"
    ))
    .maxAge("5h30m")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



