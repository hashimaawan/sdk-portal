# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQuery` | [`*models.NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/named-query-1.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getNamedQueryOutput := models.GetNamedQueryOutput{
        NamedQuery:           models.ToPointer(models.NamedQuery1{
            Name:                 "Name0",
            Description:          models.ToPointer("Description6"),
            Database:             "Database8",
            QueryString:          "QueryString2",
            NamedQueryId:         models.ToPointer("NamedQueryId2"),
            WorkGroup:            models.ToPointer("WorkGroup2"),
        }),
    }

}
```



