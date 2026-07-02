# Mongodb 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk1vbmdvZGIx

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Mongodb1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EndOfAvailability` | `*string` | Optional | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `EndOfLife` | `*string` | Optional | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `Version` | `*string` | Optional | The engine version. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    mongodb1 := models.Mongodb1{
        EndOfAvailability:     models.ToPointer("2023-05-09T00:00:00Z"),
        EndOfLife:             models.ToPointer("2023-11-09T00:00:00Z"),
        Version:               models.ToPointer("8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



