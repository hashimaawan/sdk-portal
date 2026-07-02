# List of TXT Validation Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3QlMjUyMG9mJTI1MjBUWFQlMjUyMHZhbGlkYXRpb24lMjUyMHJlY29yZA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ListOfTxtValidationRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TxtName` | `*string` | Optional, Read-only | - |
| `TxtValue` | `*string` | Optional, Read-only | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    listOfTxtValidationRecord := models.ListOfTxtValidationRecord{
        TxtName:               models.ToPointer("_acme-challenge.app.example.com"),
        TxtValue:              models.ToPointer("lXLOcN6cPv0nproViNcUHcahD9TrIPlNgdwesj0pYpk"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



