# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https


# Class Name

`LoadBalancerServiceHTTP`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Certificates` | `List<Integer>` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" | List<Integer> getCertificates() | setCertificates(List<Integer> certificates) |
| `CookieLifetime` | `Integer` | Optional | Lifetime of the cookie used for sticky sessions | Integer getCookieLifetime() | setCookieLifetime(Integer cookieLifetime) |
| `CookieName` | `String` | Optional | Name of the cookie used for sticky sessions | String getCookieName() | setCookieName(String cookieName) |
| `RedirectHttp` | `Boolean` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` | Boolean getRedirectHttp() | setRedirectHttp(Boolean redirectHttp) |
| `StickySessions` | `Boolean` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` | Boolean getStickySessions() | setStickySessions(Boolean stickySessions) |


# Example

```java
import cloud.hetzner.api.models.LoadBalancerServiceHTTP;
import java.util.Arrays;

LoadBalancerServiceHTTP loadBalancerServiceHTTP = new LoadBalancerServiceHTTP.Builder()
    .certificates(Arrays.asList(
        897
    ))
    .cookieLifetime(300)
    .cookieName("HCLBSTICKY")
    .redirectHttp(true)
    .stickySessions(true)
    .build();
```



