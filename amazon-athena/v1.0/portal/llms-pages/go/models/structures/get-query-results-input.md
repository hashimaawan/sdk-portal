# Get Query Results Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c0lucHV0


# Class Name

`GetQueryResultsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 1000` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    getQueryResultsInput := models.GetQueryResultsInput{
        QueryExecutionId:     "QueryExecutionId6",
        NextToken:            models.ToPointer("NextToken2"),
        MaxResults:           models.ToPointer(42),
    }

}
```



