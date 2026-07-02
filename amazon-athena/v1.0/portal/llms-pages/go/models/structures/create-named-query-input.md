# Create Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`CreateNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `QueryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `ClientRequestToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    createNamedQueryInput := models.CreateNamedQueryInput{
        Name:                  "Name4",
        Description:           models.ToPointer("Description0"),
        Database:              "Database4",
        QueryString:           "QueryString8",
        ClientRequestToken:    models.ToPointer("ClientRequestToken0"),
        WorkGroup:             models.ToPointer("WorkGroup8"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



