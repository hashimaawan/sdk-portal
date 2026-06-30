# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`[]models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/action.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    floatingIpsActionsResponse := models.FloatingIpsActionsResponse{
        Actions:              []models.Action{
            models.Action{
                Command:              "start_server",
                Error:                models.ToPointer(models.Error{
                    Code:                 "action_failed",
                    Message:              "Action failed",
                }),
                Finished:             models.ToPointer("2016-01-30T23:55:00+00:00"),
                Id:                   42,
                Progress:             float64(100),
                Resources:            []models.Resource{
                    models.Resource{
                        Id:                   42,
                        Type:                 "server",
                    },
                },
                Started:              "2016-01-30T23:55:00+00:00",
                Status:               models.StatusEnum_SUCCESS,
            },
        },
    }

}
```



