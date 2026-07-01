# Http

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkh0dHA

Additional configuration for protocol http


# Class Name

`Http`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Domain` | `String` | Required | Host header to send in the HTTP request. May not contain spaces, percent or backslash symbols. Can be null, in that case no host header is sent. | String getDomain() | setDomain(String domain) |
| `Path` | `String` | Required | HTTP path to use for health checks. May not contain literal spaces, use percent-encoding instead. | String getPath() | setPath(String path) |
| `Response` | `String` | Optional | String that must be contained in HTTP response in order to pass the health check | String getResponse() | setResponse(String response) |
| `StatusCodes` | `List<String>` | Optional | List of returned HTTP status codes in order to pass the health check. Supports the wildcards `?` for exactly one character and `*` for multiple ones. The default is to pass the health check for any status code between 2?? and 3??. | List<String> getStatusCodes() | setStatusCodes(List<String> statusCodes) |
| `Tls` | `Boolean` | Optional | Use HTTPS for health check | Boolean getTls() | setTls(Boolean tls) |


# Example

```java
import cloud.hetzner.api.models.Http;
import java.util.Arrays;

Http http = new Http.Builder(
    "example.com",
    "/"
)
.response("{\"status\": \"ok\"}")
.statusCodes(Arrays.asList(
        "2??",
        "3??"
    ))
.tls(false)
.build();
```



