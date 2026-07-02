# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TableMetadata` | [`*models.TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/table-metadata-2.md) | Optional | - |


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
    getTableMetadataOutput := models.GetTableMetadataOutput{
        TableMetadata:        models.ToPointer(models.TableMetadata2{
            Name:                 "Name6",
            CreateTime:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            LastAccessTime:       models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            TableType:            models.ToPointer("TableType0"),
            Columns:              []models.Column{
                models.Column{
                    Name:                 "Name0",
                    Type:                 models.ToPointer("Type0"),
                    Comment:              models.ToPointer("Comment4"),
                },
                models.Column{
                    Name:                 "Name0",
                    Type:                 models.ToPointer("Type0"),
                    Comment:              models.ToPointer("Comment4"),
                },
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
            },
        }),
    }

}
```



