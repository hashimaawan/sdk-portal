# List Notebook Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va1Nlc3Npb25zUmVxdWVzdA


# Class Name

`ListNotebookSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `MaxResults` | `*int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    listNotebookSessionsRequest := models.ListNotebookSessionsRequest{
        NotebookId:           "NotebookId8",
        MaxResults:           models.ToPointer(14),
        NextToken:            models.ToPointer("NextToken8"),
    }

}
```



