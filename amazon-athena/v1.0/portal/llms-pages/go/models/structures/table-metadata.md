# Table Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGE

Contains metadata for a table.


# Class Name

`TableMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `CreateTime` | `*time.Time` | Optional | - |
| `LastAccessTime` | `*time.Time` | Optional | - |
| `TableType` | `*string` | Optional | **Constraints**: *Maximum Length*: `255` |
| `Columns` | [`[]models.Column`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/column.md) | Optional | - |
| `PartitionKeys` | [`[]models.Column`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/column.md) | Optional | - |
| `Parameters` | [`*models.Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/parameters.md) | Optional | - |


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
    tableMetadata := models.TableMetadata{
        Name:                 "Name0",
        CreateTime:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        LastAccessTime:       models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        TableType:            models.ToPointer("TableType4"),
        Columns:              []models.Column{
            models.Column{
                Name:                 "Name0",
                Type:                 models.ToPointer("Type0"),
                Comment:              models.ToPointer("Comment4"),
            },
        },
        PartitionKeys:        []models.Column{
            models.Column{
                Name:                 "Name6",
                Type:                 models.ToPointer("Type6"),
                Comment:              models.ToPointer("Comment0"),
            },
            models.Column{
                Name:                 "Name6",
                Type:                 models.ToPointer("Type6"),
                Comment:              models.ToPointer("Comment0"),
            },
            models.Column{
                Name:                 "Name6",
                Type:                 models.ToPointer("Type6"),
                Comment:              models.ToPointer("Comment0"),
            },
        },
    }

}
```



