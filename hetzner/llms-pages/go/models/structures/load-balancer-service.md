# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DestinationPort` | `int` | Required | Port the Load Balancer will balance to |
| `HealthCheck` | [`models.LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `Http` | [`*models.LoadBalancerServiceHTTP`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `ListenPort` | `int` | Required | Port the Load Balancer listens on |
| `Protocol` | [`models.Protocol7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `Proxyprotocol` | `bool` | Required | Is Proxyprotocol enabled or not |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerService := models.LoadBalancerService{
        DestinationPort:      80,
        HealthCheck:          models.LoadBalancerServiceHealthCheck{
            Http:     models.ToPointer(models.Http{
                Domain:      models.ToPointer("domain4"),
                Path:        "path2",
                Response:    models.ToPointer("response8"),
                StatusCodes: []string{
                    "status_codes0",
                    "status_codes1",
                    "status_codes2",
                },
                Tls:         models.ToPointer(false),
            }),
            Interval: 15,
            Port:     4711,
            Protocol: models.Protocol6Enum_HTTP,
            Retries:  3,
            Timeout:  10,
        },
        Http:                 models.ToPointer(models.LoadBalancerServiceHTTP{
            Certificates:         []int{
                180,
            },
            CookieLifetime:       models.ToPointer(160),
            CookieName:           models.ToPointer("cookie_name6"),
            RedirectHttp:         models.ToPointer(false),
            StickySessions:       models.ToPointer(false),
        }),
        ListenPort:           443,
        Protocol:             models.Protocol7Enum_HTTPS,
        Proxyprotocol:        false,
    }

}
```



