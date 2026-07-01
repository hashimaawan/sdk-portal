# Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkVycm9yMg

If issuance or renewal reports `failed`, this property contains information about what happened

*This model accepts additional fields of type interface{}.*


# Class Name

`Error2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Code` | `*string` | Optional | - |
| `Message` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    error2 := models.Error2{
        Code:                  models.ToPointer("code2"),
        Message:               models.ToPointer("message4"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



