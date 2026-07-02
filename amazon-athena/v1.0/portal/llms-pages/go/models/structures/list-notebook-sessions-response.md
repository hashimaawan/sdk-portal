# List Notebook Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`ListNotebookSessionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookSessionsList` | [`[]models.NotebookSessionSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/notebook-session-summary.md) | Required | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
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
    listNotebookSessionsResponse := models.ListNotebookSessionsResponse{
        NotebookSessionsList:  []models.NotebookSessionSummary{
            models.NotebookSessionSummary{
                SessionId:             models.ToPointer("SessionId4"),
                CreationTime:          models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        NextToken:             models.ToPointer("NextToken0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



