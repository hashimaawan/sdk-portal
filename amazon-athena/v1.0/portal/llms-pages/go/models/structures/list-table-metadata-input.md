# List Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhSW5wdXQ

*This model accepts additional fields of type interface{}.*


# Class Name

`ListTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `DatabaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Expression` | `*string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` |
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
    listTableMetadataInput := models.ListTableMetadataInput{
        CatalogName:           "CatalogName2",
        DatabaseName:          "DatabaseName2",
        Expression:            models.ToPointer("Expression0"),
        NextToken:             models.ToPointer("NextToken8"),
        MaxResults:            models.ToPointer(50),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



