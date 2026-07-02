# List Work Groups Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzSW5wdXQ


# Class Name

`ListWorkGroupsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 50` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listWorkGroupsInput := models.ListWorkGroupsInput{
        NextToken:            models.ToPointer("NextToken8"),
        MaxResults:           models.ToPointer(50),
    }

}
```



