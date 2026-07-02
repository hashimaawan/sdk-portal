# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceARN` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `TagKeys` | `[]string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    untagResourceInput := models.UntagResourceInput{
        ResourceARN:          "ResourceARN6",
        TagKeys:              []string{
            "TagKeys1",
            "TagKeys2",
            "TagKeys3",
        },
    }

}
```



