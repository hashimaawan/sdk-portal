# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https


# Class Name

`LoadBalancerServiceHTTP`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `certificates` | `?(int[])` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" | getCertificates(): ?array | setCertificates(?array certificates): void |
| `cookieLifetime` | `?int` | Optional | Lifetime of the cookie used for sticky sessions | getCookieLifetime(): ?int | setCookieLifetime(?int cookieLifetime): void |
| `cookieName` | `?string` | Optional | Name of the cookie used for sticky sessions | getCookieName(): ?string | setCookieName(?string cookieName): void |
| `redirectHttp` | `?bool` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` | getRedirectHttp(): ?bool | setRedirectHttp(?bool redirectHttp): void |
| `stickySessions` | `?bool` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` | getStickySessions(): ?bool | setStickySessions(?bool stickySessions): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerServiceHTTPBuilder;

$loadBalancerServiceHTTP = LoadBalancerServiceHTTPBuilder::init()
    ->certificates(
        [
            897
        ]
    )
    ->cookieLifetime(300)
    ->cookieName('HCLBSTICKY')
    ->redirectHttp(true)
    ->stickySessions(true)
    ->build();
```



