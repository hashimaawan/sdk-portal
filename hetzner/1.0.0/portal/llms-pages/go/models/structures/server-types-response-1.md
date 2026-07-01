# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerType` | [`models.ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-type.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serverTypesResponse1 := models.ServerTypesResponse1{
        ServerType:           models.ServerType{
            Cores:                float64(1),
            CpuType:              models.CpuTypeEnum_SHARED,
            Deprecated:           false,
            Description:          "CX11",
            Disk:                 float64(24),
            Id:                   float64(1),
            Memory:               float64(1),
            Name:                 "cx11",
            Prices:               []models.Price9{
                models.Price9{
                    Location:             "fsn1",
                    PriceHourly:          models.PriceHourly8{
                        Gross:                "1.1900000000000000",
                        Net:                  "1.0000000000",
                    },
                    PriceMonthly:         models.PriceMonthly10{
                        Gross:                "1.1900000000000000",
                        Net:                  "1.0000000000",
                    },
                },
            },
            StorageType:          models.StorageTypeEnum_LOCAL,
        },
    }

}
```



