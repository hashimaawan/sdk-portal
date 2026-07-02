# List Query Executions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNJbnB1dA


# Class Name

`ListQueryExecutionsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 0`, `<= 50` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listQueryExecutionsInput := models.ListQueryExecutionsInput{
        NextToken:            models.ToPointer("NextToken2"),
        MaxResults:           models.ToPointer(34),
        WorkGroup:            models.ToPointer("WorkGroup4"),
    }

}
```



