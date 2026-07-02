# Billing History

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkJpbGxpbmdIaXN0b3J5

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`BillingHistory`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Amount` | `*string` | Optional | Amount of the billing history entry. |
| `Date` | `*time.Time` | Optional | Time the billing history entry occurred. |
| `Description` | `*string` | Optional | Description of the billing history entry. |
| `InvoiceId` | `*string` | Optional | ID of the invoice associated with the billing history entry, if  applicable. |
| `InvoiceUuid` | `*string` | Optional | UUID of the invoice associated with the billing history entry, if  applicable. |
| `Type` | [`*models.Type6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-6.md) | Optional | Type of billing history entry. |
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
    billingHistory := models.BillingHistory{
        Amount:                models.ToPointer("12.34"),
        Date:                  models.ToPointer(parseTime(time.RFC3339, "2018-06-01T08:44:38Z", func(err error) { log.Fatalln(err) })),
        Description:           models.ToPointer("Invoice for May 2018"),
        InvoiceId:             models.ToPointer("123"),
        InvoiceUuid:           models.ToPointer("example-uuid"),
        Type:                  models.ToPointer(models.Type6_Invoice),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



