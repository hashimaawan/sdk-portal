# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancerServiceHttp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificates` | `[]int` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" |
| `CookieLifetime` | `*int` | Optional | Lifetime of the cookie used for sticky sessions |
| `CookieName` | `*string` | Optional | Name of the cookie used for sticky sessions |
| `RedirectHttp` | `*bool` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` |
| `StickySessions` | `*bool` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancerServiceHttp := models.LoadBalancerServiceHttp{
        Certificates:          []int{
            897,
        },
        CookieLifetime:        models.ToPointer(300),
        CookieName:            models.ToPointer("HCLBSTICKY"),
        RedirectHttp:          models.ToPointer(true),
        StickySessions:        models.ToPointer(true),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



