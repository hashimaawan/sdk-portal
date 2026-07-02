# List Engine Versions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc0lucHV0


# Class Name

`ListEngineVersionsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 10` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listEngineVersionsInput := models.ListEngineVersionsInput{
        NextToken:            models.ToPointer("NextToken6"),
        MaxResults:           models.ToPointer(10),
    }

}
```



