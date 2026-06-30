# Load Balancer Service Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIZWFsdGhDaGVjaw

Service health check


# Class Name

`LoadBalancerServiceHealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Http` | [`*models.Http`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/http.md) | Optional | Additional configuration for protocol http |
| `Interval` | `int` | Required | Time interval in seconds health checks are performed |
| `Port` | `int` | Required | Port the health check will be performed on |
| `Protocol` | [`models.Protocol6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/protocol-6.md) | Required | Type of the health check |
| `Retries` | `int` | Required | Unsuccessful retries needed until a target is considered unhealthy; an unhealthy target needs the same number of successful retries to become healthy again |
| `Timeout` | `int` | Required | Time in seconds after an attempt is considered a timeout |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancerServiceHealthCheck := models.LoadBalancerServiceHealthCheck{
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
    }

}
```



