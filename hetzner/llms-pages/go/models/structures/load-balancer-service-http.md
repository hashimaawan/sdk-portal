# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https


# Class Name

`LoadBalancerServiceHTTP`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificates` | `[]int` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" |
| `CookieLifetime` | `*int` | Optional | Lifetime of the cookie used for sticky sessions |
| `CookieName` | `*string` | Optional | Name of the cookie used for sticky sessions |
| `RedirectHttp` | `*bool` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` |
| `StickySessions` | `*bool` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerServiceHTTP := models.LoadBalancerServiceHTTP{
        Certificates:         []int{
            897,
        },
        CookieLifetime:       models.ToPointer(300),
        CookieName:           models.ToPointer("HCLBSTICKY"),
        RedirectHttp:         models.ToPointer(true),
        StickySessions:       models.ToPointer(true),
    }

}
```



