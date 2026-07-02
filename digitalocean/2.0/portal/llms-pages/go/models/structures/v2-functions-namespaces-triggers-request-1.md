# V2 Functions Namespaces Triggers Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IsEnabled` | `*bool` | Optional | Indicates weather the trigger is paused or unpaused. |
| `ScheduledDetails` | [`*models.ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2FunctionsNamespacesTriggersRequest1 := models.V2FunctionsNamespacesTriggersRequest1{
        IsEnabled:             models.ToPointer(true),
        ScheduledDetails:      models.ToPointer(models.ScheduledDetails{
            Body:                  models.NewOptional(models.ToPointer(models.Body{
                Name:                  models.ToPointer("name6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            Cron:                  "cron2",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



