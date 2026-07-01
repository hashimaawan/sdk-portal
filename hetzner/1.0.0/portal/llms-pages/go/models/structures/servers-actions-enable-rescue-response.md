# Servers Actions Enable Rescue Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXNwb25zZQ


# Class Name

`ServersActionsEnableRescueResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`*models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Optional | - |
| `RootPassword` | `*string` | Optional | Password that will be set for this Server once the Action succeeds |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsEnableRescueResponse := models.ServersActionsEnableRescueResponse{
        Action:               models.ToPointer(models.Action{
            Command:              "command6",
            Error:                models.ToPointer(models.Error{
                Code:                 "code2",
                Message:              "message4",
            }),
            Finished:             models.ToPointer("finished0"),
            Id:                   238,
            Progress:             float64(143.26),
            Resources:            []models.Resource{
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
            },
            Started:              "started8",
            Status:               models.StatusEnum_RUNNING,
        }),
        RootPassword:         models.ToPointer("zCWbFhnu950dUTko5f40"),
    }

}
```



