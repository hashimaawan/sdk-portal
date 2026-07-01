# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    actionResponse := models.ActionResponse{
        Action:                models.Action{
            Command:               "start_server",
            Error:                 models.ToPointer(models.Error{
                Code:                  "action_failed",
                Message:               "Action failed",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Finished:              models.ToPointer("2016-01-30T23:55:00+00:00"),
            Id:                    42,
            Progress:              float64(100),
            Resources:             []models.Resource{
                models.Resource{
                    Id:                    42,
                    Type:                  "server",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Started:               "2016-01-30T23:55:00+00:00",
            Status:                models.Status_Running,
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



