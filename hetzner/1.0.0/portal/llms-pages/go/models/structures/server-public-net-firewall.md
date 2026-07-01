# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs

*This model accepts additional fields of type interface{}.*


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `*int` | Optional | ID of the Resource |
| `Status` | [`*models.Status72`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serverPublicNetFirewall := models.ServerPublicNetFirewall{
        Id:                    models.ToPointer(42),
        Status:                models.ToPointer(models.Status72_Applied),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



