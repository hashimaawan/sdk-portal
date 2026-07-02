# V2 Customers My Invoices Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InvoicePreview` | [`*models.InvoicePreview`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/invoice-preview.md) | Optional | The invoice preview. |
| `Invoices` | [`[]models.InvoicePreview`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/invoice-preview.md) | Optional | - |
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
    v2CustomersMyInvoicesResponse := models.V2CustomersMyInvoicesResponse{
        InvoicePreview:        models.ToPointer(models.InvoicePreview{
            Amount:                models.ToPointer("34.56"),
            InvoicePeriod:         models.ToPointer("2020-02"),
            InvoiceUuid:           models.ToPointer("1afe95e6-0958-4eb0-8d9a-9c5060d3ef03"),
            UpdatedAt:             models.ToPointer("2020-02-23T06:31:50Z"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Invoices:              []models.InvoicePreview{
            models.InvoicePreview{
                Amount:                models.ToPointer("12.34"),
                InvoicePeriod:         models.ToPointer("2019-12"),
                InvoiceUuid:           models.ToPointer("22737513-0ea7-4206-8ceb-98a575af7681"),
                UpdatedAt:             models.ToPointer("updated_at8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.InvoicePreview{
                Amount:                models.ToPointer("23.45"),
                InvoicePeriod:         models.ToPointer("2019-11"),
                InvoiceUuid:           models.ToPointer("fdabb512-6faf-443c-ba2e-665452332a9e"),
                UpdatedAt:             models.ToPointer("updated_at8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("https://api.digitalocean.com/v2/customers/my/invoices?page=35&per_page=2"),
                Next:                  models.ToPointer("https://api.digitalocean.com/v2/customers/my/invoices?page=2&per_page=2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 70,
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



