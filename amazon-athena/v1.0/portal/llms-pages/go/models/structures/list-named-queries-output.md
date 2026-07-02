# List Named Queries Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNPdXRwdXQ


# Class Name

`ListNamedQueriesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryIds` | `[]string` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listNamedQueriesOutput := models.ListNamedQueriesOutput{
        NamedQueryIds:        []string{
            "NamedQueryIds5",
            "NamedQueryIds4",
            "NamedQueryIds3",
        },
        NextToken:            models.ToPointer("NextToken2"),
    }

}
```



