# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DestinationPort` | `int` | Required | Port the Load Balancer will balance to |
| `HealthCheck` | [`models.LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer-service-health-check.md) | Required | Service health check |
| `Http` | [`*models.LoadBalancerServiceHttp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https |
| `ListenPort` | `int` | Required | Port the Load Balancer listens on |
| `Protocol` | [`models.Protocol7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer |
| `Proxyprotocol` | `bool` | Required | Is Proxyprotocol enabled or not |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancerService := models.LoadBalancerService{
        DestinationPort:       80,
        HealthCheck:           models.LoadBalancerServiceHealthCheck{
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
            Protocol: models.Protocol6_Http,
            Retries:  3,
            Timeout:  10,
        },
        Http:                  models.ToPointer(models.LoadBalancerServiceHttp{
            Certificates:          []int{
                180,
            },
            CookieLifetime:        models.ToPointer(160),
            CookieName:            models.ToPointer("cookie_name6"),
            RedirectHttp:          models.ToPointer(false),
            StickySessions:        models.ToPointer(false),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        ListenPort:            443,
        Protocol:              models.Protocol7_Https,
        Proxyprotocol:         false,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



