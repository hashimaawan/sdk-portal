# List Work Groups Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzSW5wdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListWorkGroupsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listWorkGroupsInput := models.ListWorkGroupsInput{
        NextToken:             models.ToPointer("NextToken8"),
        MaxResults:            models.ToPointer(50),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



