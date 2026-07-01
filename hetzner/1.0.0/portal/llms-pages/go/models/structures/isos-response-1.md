# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type interface{}.*


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Iso` | [`models.Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/iso.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    isosResponse1 := models.IsosResponse1{
        Iso:                   models.Iso{
            Deprecated:            models.ToPointer("2018-02-28T00:00:00+00:00"),
            Description:           "FreeBSD 11.0 x64",
            Id:                    42,
            Name:                  models.ToPointer("FreeBSD-11.0-RELEASE-amd64-dvd1"),
            Type:                  models.Type26_Public,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



