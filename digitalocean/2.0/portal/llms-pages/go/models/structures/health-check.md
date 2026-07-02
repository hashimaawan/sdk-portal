# Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkhlYWx0aENoZWNr

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`HealthCheck`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FailureThreshold` | `*int` | Optional | The number of failed health checks before considered unhealthy. |
| `HttpPath` | `*string` | Optional | The route path used for the HTTP health check ping. If not set, the HTTP health check will be disabled and a TCP health check used instead. |
| `InitialDelaySeconds` | `*int` | Optional | The number of seconds to wait before beginning health checks. |
| `PeriodSeconds` | `*int` | Optional | The number of seconds to wait between health checks. |
| `Port` | `*int64` | Optional | The port on which the health check will be performed. If not set, the health check will be performed on the component's http_port.<br><br>**Constraints**: `>= 1`, `<= 65535` |
| `SuccessThreshold` | `*int` | Optional | The number of successful health checks before considered healthy. |
| `TimeoutSeconds` | `*int` | Optional | The number of seconds after which the check times out. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    healthCheck := models.HealthCheck{
        FailureThreshold:      models.ToPointer(2),
        HttpPath:              models.ToPointer("/health"),
        InitialDelaySeconds:   models.ToPointer(30),
        PeriodSeconds:         models.ToPointer(60),
        Port:                  models.ToPointer(int64(80)),
        SuccessThreshold:      models.ToPointer(3),
        TimeoutSeconds:        models.ToPointer(45),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



