# Health Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkhlYWx0aCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`HealthResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Dependencies` | [`[]models.ServiceDependency`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/service-dependency.md) | Optional | - |
| `Name` | `string` | Required | - |
| `Version` | `string` | Required | The Connect server's version |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    healthResponse := models.HealthResponse{
        Dependencies:          []models.ServiceDependency{
            models.ServiceDependency{
                Message:               models.ToPointer("message6"),
                Service:               models.ToPointer("service6"),
                Status:                models.ToPointer("status8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Name:                  "name4",
        Version:               "version0",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



