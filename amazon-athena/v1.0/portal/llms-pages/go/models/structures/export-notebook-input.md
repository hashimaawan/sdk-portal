# Export Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rSW5wdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ExportNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    exportNotebookInput := models.ExportNotebookInput{
        NotebookId:            "NotebookId2",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



