# Scheduled Details

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNjaGVkdWxlZERldGFpbHM

Trigger details for SCHEDULED type, where body is optional.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ScheduledDetails`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Body` | [`models.Optional[models.Body]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/body.md) | Optional | Optional data to be sent to function while triggering the function. |
| `Cron` | `string` | Required | valid cron expression string which is required for SCHEDULED type triggers. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    scheduledDetails := models.ScheduledDetails{
        Body:                  models.NewOptional(models.ToPointer(models.Body{
            Name:                  models.ToPointer("name6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        })),
        Cron:                  "* * * * *",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



