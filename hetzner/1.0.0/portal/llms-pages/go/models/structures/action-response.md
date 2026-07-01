# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl


# Class Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    actionResponse := models.ActionResponse{
        Action:               models.Action{
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
            Status:               models.StatusEnum_RUNNING,
        },
    }

}
```



