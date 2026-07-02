# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookUrl` | `string` | Required | - |
| `AuthToken` | `string` | Required | **Constraints**: *Maximum Length*: `2048` |
| `AuthTokenExpirationTime` | `int` | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    createPresignedNotebookUrlResponse := models.CreatePresignedNotebookUrlResponse{
        NotebookUrl:             "NotebookUrl0",
        AuthToken:               "AuthToken4",
        AuthTokenExpirationTime: 240,
        AdditionalProperties:    map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



