# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ


# Class Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tags` | [`[]models.Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/tag.md) | Optional | - |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listTagsForResourceOutput := models.ListTagsForResourceOutput{
        Tags:                 []models.Tag{
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
            models.Tag{
                Key:                  models.ToPointer("Key0"),
                Value:                models.ToPointer("Value6"),
            },
        },
        NextToken:            models.ToPointer("NextToken4"),
    }

}
```



