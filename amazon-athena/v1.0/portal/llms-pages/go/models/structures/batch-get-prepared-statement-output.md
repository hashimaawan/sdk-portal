# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ


# Class Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PreparedStatements` | [`[]models.PreparedStatement`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/prepared-statement.md) | Optional | - |
| `UnprocessedPreparedStatementNames` | [`[]models.UnprocessedPreparedStatementName`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/unprocessed-prepared-statement-name.md) | Optional | - |


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
    batchGetPreparedStatementOutput := models.BatchGetPreparedStatementOutput{
        PreparedStatements:                []models.PreparedStatement{
            models.PreparedStatement{
                StatementName:        models.ToPointer("StatementName2"),
                QueryStatement:       models.ToPointer("QueryStatement6"),
                WorkGroupName:        models.ToPointer("WorkGroupName6"),
                Description:          models.ToPointer("Description2"),
                LastModifiedTime:     models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            },
            models.PreparedStatement{
                StatementName:        models.ToPointer("StatementName2"),
                QueryStatement:       models.ToPointer("QueryStatement6"),
                WorkGroupName:        models.ToPointer("WorkGroupName6"),
                Description:          models.ToPointer("Description2"),
                LastModifiedTime:     models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            },
        },
        UnprocessedPreparedStatementNames: []models.UnprocessedPreparedStatementName{
            models.UnprocessedPreparedStatementName{
                StatementName:        models.ToPointer("StatementName0"),
                ErrorCode:            models.ToPointer("ErrorCode2"),
                ErrorMessage:         models.ToPointer("ErrorMessage8"),
            },
            models.UnprocessedPreparedStatementName{
                StatementName:        models.ToPointer("StatementName0"),
                ErrorCode:            models.ToPointer("ErrorCode2"),
                ErrorMessage:         models.ToPointer("ErrorMessage8"),
            },
            models.UnprocessedPreparedStatementName{
                StatementName:        models.ToPointer("StatementName0"),
                ErrorCode:            models.ToPointer("ErrorCode2"),
                ErrorMessage:         models.ToPointer("ErrorMessage8"),
            },
        },
    }

}
```



