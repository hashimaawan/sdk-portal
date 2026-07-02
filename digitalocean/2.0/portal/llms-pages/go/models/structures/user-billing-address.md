# User Billing Address

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlVzZXJCaWxsaW5nQWRkcmVzcw

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`UserBillingAddress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddressLine1` | `*string` | Optional | Street address line 1 |
| `AddressLine2` | `*string` | Optional | Street address line 2 |
| `City` | `*string` | Optional | City |
| `CountryIso2Code` | `*string` | Optional | Country (ISO2) code |
| `CreatedAt` | `*string` | Optional | Timestamp billing address was created |
| `PostalCode` | `*string` | Optional | Postal code |
| `Region` | `*string` | Optional | Region |
| `UpdatedAt` | `*string` | Optional | Timestamp billing address was updated |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    userBillingAddress := models.UserBillingAddress{
        AddressLine1:          models.ToPointer("101 Shark Row"),
        AddressLine2:          models.ToPointer("address_line24"),
        City:                  models.ToPointer("Atlantis"),
        CountryIso2Code:       models.ToPointer("US"),
        CreatedAt:             models.ToPointer("2019-09-03T16:34:46.000+00:00"),
        PostalCode:            models.ToPointer("12345"),
        Region:                models.ToPointer("OC"),
        UpdatedAt:             models.ToPointer("2019-09-03T16:34:46.000+00:00"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



