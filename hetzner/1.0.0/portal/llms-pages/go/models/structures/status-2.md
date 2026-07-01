# Status 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXR1czI

Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates


# Class Name

`Status2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Error` | [`models.Optional[models.Error2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/error-2.md) | Optional | If issuance or renewal reports `failed`, this property contains information about what happened |
| `Issuance` | [`*models.IssuanceEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/issuance.md) | Optional | Status of the issuance process of the Certificate |
| `Renewal` | [`*models.RenewalEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/renewal.md) | Optional | Status of the renewal process of the Certificate. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    status2 := models.Status2{
        Error:                models.NewOptional[models.Error2](nil),
        Issuance:             models.ToPointer(models.IssuanceEnum_COMPLETED),
        Renewal:              models.ToPointer(models.RenewalEnum_SCHEDULED),
    }

}
```



