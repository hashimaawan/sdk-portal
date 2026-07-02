# V2 Customers My Invoices Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InvoiceItems` | [`[]models.InvoiceItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/invoice-item.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2CustomersMyInvoicesResponse1 := models.V2CustomersMyInvoicesResponse1{
        InvoiceItems:          []models.InvoiceItem{
            models.InvoiceItem{
                Amount:                models.ToPointer("12.34"),
                Description:           models.ToPointer("a56e086a317d8410c8b4cfd1f4dc9f82"),
                Duration:              models.ToPointer("744"),
                DurationUnit:          models.ToPointer("Hours"),
                EndTime:               models.ToPointer("2020-02-01T00:00:00Z"),
                GroupDescription:      models.ToPointer("my-doks-cluster"),
                Product:               models.ToPointer("Kubernetes Clusters"),
                ResourceUuid:          models.ToPointer("711157cb-37c8-4817-b371-44fa3504a39c"),
                StartTime:             models.ToPointer("2020-01-01T00:00:00Z"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.InvoiceItem{
                Amount:                models.ToPointer("34.45"),
                Description:           models.ToPointer("Spaces ($5/mo 250GB storage & 1TB bandwidth)"),
                Duration:              models.ToPointer("744"),
                DurationUnit:          models.ToPointer("Hours"),
                EndTime:               models.ToPointer("2020-02-01T00:00:00Z"),
                Product:               models.ToPointer("Spaces Subscription"),
                StartTime:             models.ToPointer("2020-01-01T00:00:00Z"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=3&per_page=2"),
                Next:                  models.ToPointer("https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=2&per_page=2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 6,
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



