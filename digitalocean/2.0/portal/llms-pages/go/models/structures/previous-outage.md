# Previous Outage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlByZXZpb3VzT3V0YWdl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`PreviousOutage`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DurationSeconds` | `*int` | Optional | - |
| `EndedAt` | `*string` | Optional | - |
| `Region` | `*string` | Optional | - |
| `StartedAt` | `*string` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    previousOutage := models.PreviousOutage{
        DurationSeconds:       models.ToPointer(120),
        EndedAt:               models.ToPointer("2022-03-17T18:06:55Z"),
        Region:                models.ToPointer("us_east"),
        StartedAt:             models.ToPointer("2022-03-17T18:04:55Z"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



