# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null

*This model accepts additional fields of type interface{}.*


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Code` | `string` | Required | Fixed machine readable code |
| `Message` | `string` | Required | Humanized error message |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    mError := models.Error{
        Code:                  "action_failed",
        Message:               "Action failed",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



