# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Rules` | [`[]models.Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    setRulesRequest := models.SetRulesRequest{
        Rules:                []models.Rule{
            models.Rule{
                Description:          models.NewOptional(models.ToPointer("description2")),
                DestinationIps:       []string{
                    "28.239.13.1/32",
                    "28.239.14.0/24",
                    "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                },
                Direction:            models.DirectionEnum_IN,
                Port:                 models.ToPointer("80"),
                Protocol:             models.ProtocolEnum_UDP,
                SourceIps:            []string{
                    "28.239.13.1/32",
                    "28.239.14.0/24",
                    "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                },
            },
        },
    }

}
```



