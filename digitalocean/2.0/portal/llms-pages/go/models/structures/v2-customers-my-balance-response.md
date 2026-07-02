# V2 Customers My Balance Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCYWxhbmNlJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2CustomersMyBalanceResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AccountBalance` | `*string` | Optional | Current balance of the customer's most recent billing activity.  Does not reflect `month_to_date_usage`. |
| `GeneratedAt` | `*time.Time` | Optional | The time at which balances were most recently generated. |
| `MonthToDateBalance` | `*string` | Optional | Balance as of the `generated_at` time.  This value includes the `account_balance` and `month_to_date_usage`. |
| `MonthToDateUsage` | `*string` | Optional | Amount used in the current billing period as of the `generated_at` time. |
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
    v2CustomersMyBalanceResponse := models.V2CustomersMyBalanceResponse{
        AccountBalance:        models.ToPointer("12.23"),
        GeneratedAt:           models.ToPointer(parseTime(time.RFC3339, "2019-07-09T15:01:12Z", func(err error) { log.Fatalln(err) })),
        MonthToDateBalance:    models.ToPointer("23.44"),
        MonthToDateUsage:      models.ToPointer("11.21"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



