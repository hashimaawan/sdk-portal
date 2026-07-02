# Create Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`CreateNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    createNamedQueryOutput := models.CreateNamedQueryOutput{
        NamedQueryId:          models.ToPointer("NamedQueryId0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



