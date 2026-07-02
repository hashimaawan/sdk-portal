# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TableMetadataList` | [`[]models.TableMetadata`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/table-metadata.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


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
    listTableMetadataOutput := models.ListTableMetadataOutput{
        TableMetadataList:    []models.TableMetadata{
            models.TableMetadata{
                Name:                 "Name2",
                CreateTime:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                LastAccessTime:       models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                TableType:            models.ToPointer("TableType2"),
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
            },
            models.TableMetadata{
                Name:                 "Name2",
                CreateTime:           models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                LastAccessTime:       models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                TableType:            models.ToPointer("TableType2"),
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
            },
        },
        NextToken:            models.ToPointer("NextToken0"),
    }

}
```



