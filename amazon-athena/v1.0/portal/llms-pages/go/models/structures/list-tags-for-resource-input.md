# List Tags for Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`ListTagsForResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 75` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listTagsForResourceInput := models.ListTagsForResourceInput{
        ResourceArn:           "ResourceARN0",
        NextToken:             models.ToPointer("NextToken0"),
        MaxResults:            models.ToPointer(76),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



