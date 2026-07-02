# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ


# Class Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `Payload` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `Type` | [`models.NotebookType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/notebook-type-2.md) | Required | - |
| `ClientRequestToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    importNotebookInput := models.ImportNotebookInput{
        WorkGroup:            "WorkGroup2",
        Name:                 "Name0",
        Payload:              "Payload6",
        Type:                 models.NotebookType2Enum_IPYNB,
        ClientRequestToken:   models.ToPointer("ClientRequestToken4"),
    }

}
```



