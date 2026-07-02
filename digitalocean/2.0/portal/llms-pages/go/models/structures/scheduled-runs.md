# Scheduled Runs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNjaGVkdWxlZFJ1bnM

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ScheduledRuns`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LastRunAt` | `models.Optional[string]` | Optional | Indicates last run time. null value indicates trigger not run yet. |
| `NextRunAt` | `models.Optional[string]` | Optional | Indicates next run time. null value indicates trigger will not run. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    scheduledRuns := models.ScheduledRuns{
        LastRunAt:             models.NewOptional(models.ToPointer("2022-11-11T04:16:45Z")),
        NextRunAt:             models.NewOptional(models.ToPointer("2022-11-11T04:16:45Z")),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



