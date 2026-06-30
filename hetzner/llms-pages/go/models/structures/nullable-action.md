# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Command` | `string` | Required | Command executed in the Action |
| `Error` | [`*models.Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null |
| `Finished` | `*string` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. |
| `Id` | `int` | Required | ID of the Resource |
| `Progress` | `float64` | Required | Progress of Action in percent |
| `Resources` | [`[]models.Resource`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/resource.md) | Required | Resources the Action relates to |
| `Started` | `string` | Required | Point in time when the Action was started (in ISO-8601 format) |
| `Status` | [`models.StatusEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/status.md) | Required | Status of the Action |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    nullableAction := models.NullableAction{
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
    }

}
```



