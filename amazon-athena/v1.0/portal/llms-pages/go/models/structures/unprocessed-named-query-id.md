# Unprocessed Named Query Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkTmFtZWRRdWVyeUlk

Information about a named query ID that could not be processed.


# Class Name

`UnprocessedNamedQueryId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `ErrorCode` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ErrorMessage` | `*string` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    unprocessedNamedQueryId := models.UnprocessedNamedQueryId{
        NamedQueryId:         models.ToPointer("NamedQueryId0"),
        ErrorCode:            models.ToPointer("ErrorCode8"),
        ErrorMessage:         models.ToPointer("ErrorMessage8"),
    }

}
```



