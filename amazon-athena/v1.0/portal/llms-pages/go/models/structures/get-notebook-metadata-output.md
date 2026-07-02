# Get Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFPdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`GetNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookMetadata` | [`*models.NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/notebook-metadata-1.md) | Optional | - |
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
    getNotebookMetadataOutput := models.GetNotebookMetadataOutput{
        NotebookMetadata:      models.ToPointer(models.NotebookMetadata1{
            NotebookId:            models.ToPointer("NotebookId0"),
            Name:                  models.ToPointer("Name0"),
            WorkGroup:             models.ToPointer("WorkGroup2"),
            CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            Type:                  models.ToPointer(models.NotebookType1_Ipynb),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



