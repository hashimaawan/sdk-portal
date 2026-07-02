# Create Presigned Notebook Url Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`CreatePresignedNotebookUrlRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    createPresignedNotebookUrlRequest := models.CreatePresignedNotebookUrlRequest{
        SessionId:             "SessionId0",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



