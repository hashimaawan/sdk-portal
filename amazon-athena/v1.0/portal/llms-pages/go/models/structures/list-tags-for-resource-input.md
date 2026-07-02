# List Tags for Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VJbnB1dA


# Class Name

`ListTagsForResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceARN` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 75` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listTagsForResourceInput := models.ListTagsForResourceInput{
        ResourceARN:          "ResourceARN0",
        NextToken:            models.ToPointer("NextToken0"),
        MaxResults:           models.ToPointer(76),
    }

}
```



