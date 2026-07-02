# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQuery` | [`*models.NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/named-query-1.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    getNamedQueryOutput := models.GetNamedQueryOutput{
        NamedQuery:            models.ToPointer(models.NamedQuery1{
            Name:                  "Name0",
            Description:           models.ToPointer("Description6"),
            Database:              "Database8",
            QueryString:           "QueryString2",
            NamedQueryId:          models.ToPointer("NamedQueryId2"),
            WorkGroup:             models.ToPointer("WorkGroup2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



