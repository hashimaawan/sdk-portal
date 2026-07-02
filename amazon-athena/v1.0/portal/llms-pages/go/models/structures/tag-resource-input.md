# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceARN` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `Tags` | [`[]models.Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/tag.md) | Required | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    tagResourceInput := models.TagResourceInput{
        ResourceARN:          "ResourceARN6",
        Tags:                 []models.Tag{
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
        },
    }

}
```



