# Named Query 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRk5hbWVkUXVlcnkx


# Class Name

`NamedQuery1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `NamedQueryId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    namedQuery1 := models.NamedQuery1{
        Name:                 "Name0",
        Description:          models.ToPointer("Description6"),
        Database:             "Database8",
        QueryString:          "QueryString2",
        NamedQueryId:         models.ToPointer("NamedQueryId2"),
        WorkGroup:            models.ToPointer("WorkGroup2"),
    }

}
```



