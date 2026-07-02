# Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRk5hbWVkUXVlcnk

A query, where <code>QueryString</code> contains the SQL statements that make up the query.

*This model accepts additional fields of type interface{}.*


# Class Name

`NamedQuery`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `NamedQueryId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    namedQuery := models.NamedQuery{
        Name:                  "Name8",
        Description:           models.ToPointer("Description4"),
        Database:              "Database0",
        QueryString:           "QueryString4",
        NamedQueryId:          models.ToPointer("NamedQueryId0"),
        WorkGroup:             models.ToPointer("WorkGroup4"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



