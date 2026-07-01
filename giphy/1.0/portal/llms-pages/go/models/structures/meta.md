# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0bSUyRk1ldGE

The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances.

*This model accepts additional fields of type interface{}.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Msg` | `*string` | Optional | HTTP Response Message |
| `ResponseId` | `*string` | Optional | A unique ID paired with this response from the API. |
| `Status` | `*int` | Optional | HTTP Response Code |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "giphyApi/models"
)

func main() {
    meta := models.Meta{
        Msg:                   models.ToPointer("OK"),
        ResponseId:            models.ToPointer("57eea03c72381f86e05c35d2"),
        Status:                models.ToPointer(200),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



