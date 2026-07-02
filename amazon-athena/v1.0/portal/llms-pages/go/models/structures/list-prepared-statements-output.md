# List Prepared Statements Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNPdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListPreparedStatementsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PreparedStatements` | [`[]models.PreparedStatementSummary`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/prepared-statement-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
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
    listPreparedStatementsOutput := models.ListPreparedStatementsOutput{
        PreparedStatements:    []models.PreparedStatementSummary{
            models.PreparedStatementSummary{
                StatementName:         models.ToPointer("StatementName2"),
                LastModifiedTime:      models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.PreparedStatementSummary{
                StatementName:         models.ToPointer("StatementName2"),
                LastModifiedTime:      models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        NextToken:             models.ToPointer("NextToken2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



