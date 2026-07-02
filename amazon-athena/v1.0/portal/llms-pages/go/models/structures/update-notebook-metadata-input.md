# Update Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdateNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `ClientRequestToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    updateNotebookMetadataInput := models.UpdateNotebookMetadataInput{
        NotebookId:            "NotebookId8",
        ClientRequestToken:    models.ToPointer("ClientRequestToken2"),
        Name:                  "Name8",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



