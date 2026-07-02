# Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlRpZXI

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Tier`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BuildSeconds` | `*string` | Optional | - |
| `EgressBandwidthBytes` | `*string` | Optional | - |
| `Name` | `*string` | Optional | - |
| `Slug` | `*string` | Optional | - |
| `StorageBytes` | `*string` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    tier := models.Tier{
        BuildSeconds:          models.ToPointer("233"),
        EgressBandwidthBytes:  models.ToPointer("123"),
        Name:                  models.ToPointer("test"),
        Slug:                  models.ToPointer("test"),
        StorageBytes:          models.ToPointer("10000000"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



