# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookMetadata` | [`*models.NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/notebook-metadata-1.md) | Optional | - |
| `Payload` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |


# Example

```go
package main

import (
    "log"
    "time"
    "amazonathena/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    exportNotebookOutput := models.ExportNotebookOutput{
        NotebookMetadata:     models.ToPointer(models.NotebookMetadata1{
            NotebookId:           models.ToPointer("NotebookId0"),
            Name:                 models.ToPointer("Name0"),
            WorkGroup:            models.ToPointer("WorkGroup2"),
            CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            Type:                 models.ToPointer(models.NotebookType1Enum_IPYNB),
        }),
        Payload:              models.ToPointer("Payload2"),
    }

}
```



