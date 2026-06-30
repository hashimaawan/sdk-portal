# API Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkFQSVJlcXVlc3Q

Represents a request that was made to the API. Including what Token was used and what resource was accessed.

*This model accepts additional fields of type interface{}.*


# Class Name

`ApiRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`*models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/action.md) | Optional | - |
| `Actor` | [`*models.Actor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/actor.md) | Optional | - |
| `RequestId` | `*uuid.UUID` | Optional | The unique id used to identify a single request. |
| `Resource` | [`*models.Resource`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/resource.md) | Optional | - |
| `Result` | [`*models.Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/result.md) | Optional | - |
| `Timestamp` | `*time.Time` | Optional, Read-only | The time at which the request was processed by the server. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
    "github.com/google/uuid"
)

func main() {
    apiRequest := models.ApiRequest{
        Action:                models.ToPointer(models.Action_Read),
        Actor:                 models.ToPointer(models.Actor{
            Account:               models.ToPointer("account0"),
            Id:                    models.ToPointer(uuid.MustParse("0000193c-0000-0000-0000-000000000000")),
            Jti:                   models.ToPointer("jti2"),
            RequestIp:             models.ToPointer("requestIp4"),
            UserAgent:             models.ToPointer("userAgent6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        RequestId:             models.ToPointer(uuid.MustParse("000002a8-0000-0000-0000-000000000000")),
        Resource:              models.ToPointer(models.Resource{
            Item:                  models.ToPointer(models.Item2{
                Id:                    models.ToPointer("id2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            ItemVersion:           models.ToPointer(108),
            Type:                  models.ToPointer(models.Type_Item),
            Vault:                 models.ToPointer(models.Vault3{
                Id:                    models.ToPointer("id6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Result:                models.ToPointer(models.Result_Success),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



