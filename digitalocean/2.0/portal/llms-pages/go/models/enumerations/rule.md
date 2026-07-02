# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJ1bGU


# Class Name

`Rule`


# Fields

| Name |
|  --- |
| `UnspecifiedRule` |
| `CpuUtilization` |
| `MemUtilization` |
| `RestartCount` |
| `DeploymentFailed` |
| `DeploymentLive` |
| `DomainFailed` |
| `DomainLive` |
| `FunctionsActivationCount` |
| `FunctionsAverageDurationMs` |
| `FunctionsErrorRatePerMinute` |
| `FunctionsAverageWaitTimeMs` |
| `FunctionsErrorCount` |
| `FunctionsGbRatePerSecond` |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    rule := models.Rule_FunctionsErrorRatePerMinute

}
```



