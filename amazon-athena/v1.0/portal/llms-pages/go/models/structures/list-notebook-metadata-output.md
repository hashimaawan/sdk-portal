# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0

*This model accepts additional fields of type interface{}.*


# Class Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `NotebookMetadataList` | [`[]models.NotebookMetadata`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/notebook-metadata.md) | Optional | - |
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
    listNotebookMetadataOutput := models.ListNotebookMetadataOutput{
        NextToken:             models.ToPointer("NextToken2"),
        NotebookMetadataList:  []models.NotebookMetadata{
            models.NotebookMetadata{
                NotebookId:            models.ToPointer("NotebookId4"),
                Name:                  models.ToPointer("Name4"),
                WorkGroup:             models.ToPointer("WorkGroup6"),
                CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                Type:                  models.ToPointer(models.NotebookType1_Ipynb),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



