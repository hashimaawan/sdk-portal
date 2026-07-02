# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DatabaseList` | [`[]models.Database`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/database.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listDatabasesOutput := models.ListDatabasesOutput{
        DatabaseList:         []models.Database{
            models.Database{
                Name:                 "Name4",
                Description:          models.ToPointer("Description8"),
                Parameters:           models.ToPointer(models.Parameters{
                }),
            },
            models.Database{
                Name:                 "Name4",
                Description:          models.ToPointer("Description8"),
                Parameters:           models.ToPointer(models.Parameters{
                }),
            },
            models.Database{
                Name:                 "Name4",
                Description:          models.ToPointer("Description8"),
                Parameters:           models.ToPointer(models.Parameters{
                }),
            },
        },
        NextToken:            models.ToPointer("NextToken6"),
    }

}
```



