# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Available` | `[]float64` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `AvailableForMigration` | `[]float64` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `Supported` | `[]float64` | Required | IDs of Server types that are supported in the Datacenter |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serverTypes := models.ServerTypes{
        Available:             []float64{
            float64(1),
            float64(2),
            float64(3),
        },
        AvailableForMigration: []float64{
            float64(1),
            float64(2),
            float64(3),
        },
        Supported:             []float64{
            float64(1),
            float64(2),
            float64(3),
        },
    }

}
```



