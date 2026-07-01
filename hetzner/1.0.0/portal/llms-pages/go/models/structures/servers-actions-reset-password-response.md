# Servers Actions Reset Password Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlc2V0JTI1MjBQYXNzd29yZCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`ServersActionsResetPasswordResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`*models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Optional | - |
| `RootPassword` | `*string` | Optional | Password that will be set for this Server once the Action succeeds |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serversActionsResetPasswordResponse := models.ServersActionsResetPasswordResponse{
        Action:                models.ToPointer(models.Action{
            Command:               "command6",
            Error:                 models.ToPointer(models.Error{
                Code:                  "code2",
                Message:               "message4",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Finished:              models.ToPointer("finished0"),
            Id:                    238,
            Progress:              float64(143.26),
            Resources:             []models.Resource{
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Started:               "started8",
            Status:                models.Status_Running,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        RootPassword:          models.ToPointer("zCWbFhnu950dUTko5f40"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



