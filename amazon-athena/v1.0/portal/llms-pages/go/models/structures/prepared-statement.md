# Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50

A prepared SQL statement for use with Athena.

*This model accepts additional fields of type interface{}.*


# Class Name

`PreparedStatement`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatementName` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `QueryStatement` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `WorkGroupName` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
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
    preparedStatement := models.PreparedStatement{
        StatementName:         models.ToPointer("StatementName8"),
        QueryStatement:        models.ToPointer("QueryStatement2"),
        WorkGroupName:         models.ToPointer("WorkGroupName2"),
        Description:           models.ToPointer("Description4"),
        LastModifiedTime:      models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



