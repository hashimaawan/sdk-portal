# Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFjdGlvbnNSZXNwb25zZQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`[]models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    actionsResponse := models.ActionsResponse{
        Actions:               []models.Action{
            models.Action{
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
                Status:                models.Status_Success,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Meta:                  models.ToPointer(models.Meta{
            Pagination:            models.Pagination{
                LastPage:              models.ToPointer(float64(77.7)),
                NextPage:              models.ToPointer(float64(209.18)),
                Page:                  float64(17.58),
                PerPage:               float64(13.34),
                PreviousPage:          models.ToPointer(float64(50.02)),
                TotalEntries:          models.ToPointer(float64(206.64)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
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



