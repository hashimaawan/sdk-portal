# Trigger

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlRyaWdnZXI

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Trigger`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*string` | Optional | UTC time string. |
| `Function` | `*string` | Optional | Name of function(action) that exists in the given namespace. |
| `IsEnabled` | `*bool` | Optional | Indicates weather the trigger is paused or unpaused. |
| `Name` | `*string` | Optional | The trigger's unique name within the namespace. |
| `Namespace` | `*string` | Optional | A unique string format of UUID with a prefix fn-. |
| `ScheduledDetails` | [`*models.ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/scheduled-details.md) | Optional | Trigger details for SCHEDULED type, where body is optional. |
| `ScheduledRuns` | [`*models.ScheduledRuns`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/scheduled-runs.md) | Optional | - |
| `Type` | `*string` | Optional | String which indicates the type of trigger source like SCHEDULED. |
| `UpdatedAt` | `*string` | Optional | UTC time string. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    trigger := models.Trigger{
        CreatedAt:             models.ToPointer("2022-11-11T04:16:45Z"),
        Function:              models.ToPointer("hello"),
        IsEnabled:             models.ToPointer(true),
        Name:                  models.ToPointer("my trigger"),
        Namespace:             models.ToPointer("fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"),
        Type:                  models.ToPointer("SCHEDULED"),
        UpdatedAt:             models.ToPointer("2022-11-11T04:16:45Z"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



