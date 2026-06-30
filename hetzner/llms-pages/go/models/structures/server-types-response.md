# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerTypes` | [`[]models.ServerTypes7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/server-types-7.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serverTypesResponse := models.ServerTypesResponse{
        ServerTypes:          []models.ServerTypes7{
            models.ServerTypes7{
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
        },
    }

}
```



