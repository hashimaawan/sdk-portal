# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Rules` | [`[]models.Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    setRulesRequest := models.SetRulesRequest{
        Rules:                 []models.Rule{
            models.Rule{
                Description:           models.NewOptional(models.ToPointer("description2")),
                DestinationIps:        []string{
                    "28.239.13.1/32",
                    "28.239.14.0/24",
                    "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                },
                Direction:             models.Direction_In,
                Port:                  models.ToPointer("80"),
                Protocol:              models.Protocol_Udp,
                SourceIps:             []string{
                    "28.239.13.1/32",
                    "28.239.14.0/24",
                    "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



