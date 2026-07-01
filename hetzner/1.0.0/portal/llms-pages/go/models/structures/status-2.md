# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates

*This model accepts additional fields of type interface{}.*


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`models.Optional[models.Error2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened |
| `Issuance` | [`*models.Issuance`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate |
| `Renewal` | [`*models.Renewal`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    status2 := models.Status2{
        Error:                 models.NewOptional[models.Error2](nil),
        Issuance:              models.ToPointer(models.Issuance_Completed),
        Renewal:               models.ToPointer(models.Renewal_Scheduled),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



