# V2 Functions Namespaces Triggers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Function` | `string` | Required | Name of function(action) that exists in the given namespace. |
| `IsEnabled` | `bool` | Required | Indicates weather the trigger is paused or unpaused. |
| `Name` | `string` | Required | The trigger's unique name within the namespace. |
| `ScheduledDetails` | [`models.ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/scheduled-details.md) | Required | Trigger details for SCHEDULED type, where body is optional. |
| `Type` | `string` | Required | One of different type of triggers. Currently only SCHEDULED is supported. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2FunctionsNamespacesTriggersRequest := models.V2FunctionsNamespacesTriggersRequest{
        Function:              "hello",
        IsEnabled:             true,
        Name:                  "my trigger",
        ScheduledDetails:      models.ScheduledDetails{
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
        },
        Type:                  "SCHEDULED",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



