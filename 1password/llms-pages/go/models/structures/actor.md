# Actor

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkFjdG9y

*This model accepts additional fields of type interface{}.*


# Class Name

`Actor`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Account` | `*string` | Optional | - |
| `Id` | `*uuid.UUID` | Optional | - |
| `Jti` | `*string` | Optional | - |
| `RequestIp` | `*string` | Optional | - |
| `UserAgent` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
    "github.com/google/uuid"
)

func main() {
    actor := models.Actor{
        Account:               models.ToPointer("account0"),
        Id:                    models.ToPointer(uuid.MustParse("0000193c-0000-0000-0000-000000000000")),
        Jti:                   models.ToPointer("jti2"),
        RequestIp:             models.ToPointer("requestIp4"),
        UserAgent:             models.ToPointer("userAgent6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



