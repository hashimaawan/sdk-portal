# Markets

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRk1hcmtldHM

*This model accepts additional fields of type interface{}.*


# Class Name

`Markets`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Markets` | `[]string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    markets := models.Markets{
        Markets:               []string{
            "CA",
            "BR",
            "IT",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



