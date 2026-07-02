# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `StateFilter` | [`*models.SessionState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/session-state-3.md) | Optional | - |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `*string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listSessionsRequest := models.ListSessionsRequest{
        WorkGroup:             "WorkGroup8",
        StateFilter:           models.ToPointer(models.SessionState3_Creating),
        MaxResults:            models.ToPointer(100),
        NextToken:             models.ToPointer("NextToken6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



