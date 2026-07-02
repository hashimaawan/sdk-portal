# V2 Customers My Invoices Summary Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwU3VtbWFyeSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesSummaryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Amount` | `*string` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `BillingPeriod` | `*string` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `CreditsAndAdjustments` | [`*models.CreditsAndAdjustments`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/credits-and-adjustments.md) | Optional | - |
| `InvoiceUuid` | `*string` | Optional | UUID of the invoice |
| `Overages` | [`*models.Overages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/overages.md) | Optional | - |
| `ProductCharges` | [`*models.ProductCharges`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/product-charges.md) | Optional | - |
| `Taxes` | [`*models.Taxes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/taxes.md) | Optional | - |
| `UserBillingAddress` | [`*models.UserBillingAddress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/user-billing-address.md) | Optional | - |
| `UserCompany` | `*string` | Optional | Company of the DigitalOcean customer being invoiced, if set. |
| `UserEmail` | `*string` | Optional | Email of the DigitalOcean customer being invoiced. |
| `UserName` | `*string` | Optional | Name of the DigitalOcean customer being invoiced. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2CustomersMyInvoicesSummaryResponse := models.V2CustomersMyInvoicesSummaryResponse{
        Amount:                models.ToPointer("27.13"),
        BillingPeriod:         models.ToPointer("2020-01"),
        CreditsAndAdjustments: models.ToPointer(models.CreditsAndAdjustments{
            Amount:                models.ToPointer("amount6"),
            Name:                  models.ToPointer("name4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        InvoiceUuid:           models.ToPointer("22737513-0ea7-4206-8ceb-98a575af7681"),
        Overages:              models.ToPointer(models.Overages{
            Amount:                models.ToPointer("amount6"),
            Name:                  models.ToPointer("name4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        UserCompany:           models.ToPointer("DigitalOcean"),
        UserEmail:             models.ToPointer("sammy@digitalocean.com"),
        UserName:              models.ToPointer("Sammy Shark"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



