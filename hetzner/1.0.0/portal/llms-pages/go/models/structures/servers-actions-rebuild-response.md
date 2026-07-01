# Servers Actions Rebuild Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlYnVpbGQlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsRebuildResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`*models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Optional | - |
| `RootPassword` | `models.Optional[string]` | Optional | New root password when not using SSH keys |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsRebuildResponse := models.ServersActionsRebuildResponse{
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
        RootPassword:         models.NewOptional(models.ToPointer("root_password6")),
    }

}
```



