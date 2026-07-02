# List Named Queries Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNJbnB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`ListNamedQueriesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 0`, `<= 50` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listNamedQueriesInput := models.ListNamedQueriesInput{
        NextToken:             models.ToPointer("NextToken8"),
        MaxResults:            models.ToPointer(50),
        WorkGroup:             models.ToPointer("WorkGroup0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



