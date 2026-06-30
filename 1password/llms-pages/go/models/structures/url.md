# Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlVybA

*This model accepts additional fields of type interface{}.*


# Class Name

`Url`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `string` | Required | - |
| `Label` | `*string` | Optional | - |
| `Primary` | `*bool` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    url := models.Url{
        Href:                  "href6",
        Label:                 models.ToPointer("label4"),
        Primary:               models.ToPointer(false),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



