# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `TagKeys` | `[]string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    untagResourceInput := models.UntagResourceInput{
        ResourceArn:           "ResourceARN6",
        TagKeys:               []string{
            "TagKeys1",
            "TagKeys2",
            "TagKeys3",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



