# Update Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdateNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    updateNamedQueryInput := models.UpdateNamedQueryInput{
        NamedQueryId:          "NamedQueryId8",
        Name:                  "Name4",
        Description:           models.ToPointer("Description2"),
        QueryString:           "QueryString6",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



