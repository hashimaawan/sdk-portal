# Notebook Metadata 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGEx


# Class Name

`NotebookMetadata1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `Name` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `CreationTime` | `*time.Time` | Optional | - |
| `Type` | [`*models.NotebookType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/notebook-type-1.md) | Optional | - |
| `LastModifiedTime` | `*time.Time` | Optional | - |


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
    notebookMetadata1 := models.NotebookMetadata1{
        NotebookId:           models.ToPointer("NotebookId2"),
        Name:                 models.ToPointer("Name2"),
        WorkGroup:            models.ToPointer("WorkGroup4"),
        CreationTime:         models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Type:                 models.ToPointer(models.NotebookType1Enum_IPYNB),
    }

}
```



