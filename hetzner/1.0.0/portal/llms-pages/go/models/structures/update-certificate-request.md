# Update Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZUNlcnRpZmljYXRlUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New Certificate name |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    updateCertificateRequest := models.UpdateCertificateRequest{
        Labels:                models.ToPointer(interface{}("[labelkey, value]")),
        Name:                  models.ToPointer("my website cert"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



