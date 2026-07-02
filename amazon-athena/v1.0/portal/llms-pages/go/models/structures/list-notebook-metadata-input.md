# List Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Filters` | [`*models.Filters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/filters.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listNotebookMetadataInput := models.ListNotebookMetadataInput{
        Filters:               models.ToPointer(models.Filters{
            Name:                  models.ToPointer("Name2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        NextToken:             models.ToPointer("NextToken2"),
        MaxResults:            models.ToPointer(50),
        WorkGroup:             "WorkGroup4",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



