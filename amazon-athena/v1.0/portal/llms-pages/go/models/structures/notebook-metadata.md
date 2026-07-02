# Notebook Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGE

Contains metadata for notebook, including the notebook name, ID, workgroup, and time created.

*This model accepts additional fields of type interface{}.*


# Class Name

`NotebookMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `Name` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `CreationTime` | `*time.Time` | Optional | - |
| `Type` | [`*models.NotebookType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/notebook-type-1.md) | Optional | - |
| `LastModifiedTime` | `*time.Time` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "amazonAthena/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    notebookMetadata := models.NotebookMetadata{
        NotebookId:            models.ToPointer("NotebookId0"),
        Name:                  models.ToPointer("Name0"),
        WorkGroup:             models.ToPointer("WorkGroup2"),
        CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Type:                  models.ToPointer(models.NotebookType1_Ipynb),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



