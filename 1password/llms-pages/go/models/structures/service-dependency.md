# Service Dependency

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlNlcnZpY2VEZXBlbmRlbmN5

The state of a registered server dependency.

*This model accepts additional fields of type interface{}.*


# Class Name

`ServiceDependency`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Message` | `*string` | Optional | Human-readable message for explaining the current state. |
| `Service` | `*string` | Optional | - |
| `Status` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    serviceDependency := models.ServiceDependency{
        Message:               models.ToPointer("message6"),
        Service:               models.ToPointer("service6"),
        Status:                models.ToPointer("status8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



