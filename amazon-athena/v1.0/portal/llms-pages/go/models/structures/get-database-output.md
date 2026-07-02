# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | [`*models.Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/database-2.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getDatabaseOutput := models.GetDatabaseOutput{
        Database:             models.ToPointer(models.Database2{
            Name:                 "Name2",
            Description:          models.ToPointer("Description8"),
            Parameters:           models.ToPointer(models.Parameters{
            }),
        }),
    }

}
```



