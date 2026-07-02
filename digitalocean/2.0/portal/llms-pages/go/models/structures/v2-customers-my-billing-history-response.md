# V2 Customers My Billing History Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCaWxsaW5nJTI1MjBIaXN0b3J5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2CustomersMyBillingHistoryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BillingHistory` | [`[]models.BillingHistory`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/billing-history.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta-1.md) | Required | Information about the response itself. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    v2CustomersMyBillingHistoryResponse := models.V2CustomersMyBillingHistoryResponse{
        BillingHistory:        []models.BillingHistory{
            models.BillingHistory{
                Amount:                models.ToPointer("12.34"),
                Date:                  models.ToPointer(parseTime(time.RFC3339, "2018-06-01T08:44:38Z", func(err error) { log.Fatalln(err) })),
                Description:           models.ToPointer("Invoice for May 2018"),
                InvoiceId:             models.ToPointer("123"),
                InvoiceUuid:           models.ToPointer("example-uuid"),
                Type:                  models.ToPointer(models.Type6_Invoice),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.BillingHistory{
                Amount:                models.ToPointer("-12.34"),
                Date:                  models.ToPointer(parseTime(time.RFC3339, "2018-06-02T08:44:38Z", func(err error) { log.Fatalln(err) })),
                Description:           models.ToPointer("Payment (MC 2018)"),
                InvoiceId:             models.ToPointer("invoice_id6"),
                InvoiceUuid:           models.ToPointer("invoice_uuid4"),
                Type:                  models.ToPointer(models.Type6_Payment),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("https://api.digitalocean.com/v2/customers/my/billing_history?page=3&per_page=2"),
                Next:                  models.ToPointer("https://api.digitalocean.com/v2/customers/my/billing_history?page=2&per_page=2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta1{
            Total:                 models.ToPointer(5),
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



