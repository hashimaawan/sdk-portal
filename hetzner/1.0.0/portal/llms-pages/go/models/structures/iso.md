# Iso

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklzbw


# Class Name

`Iso`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Deprecated` | `*string` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `Description` | `string` | Required | Description of the ISO |
| `Id` | `int` | Required | ID of the Resource |
| `Name` | `*string` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `Type` | [`models.Type26Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-26.md) | Required | Type of the ISO |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    iso := models.Iso{
        Deprecated:           models.ToPointer("2018-02-28T00:00:00+00:00"),
        Description:          "FreeBSD 11.0 x64",
        Id:                   42,
        Name:                 models.ToPointer("FreeBSD-11.0-RELEASE-amd64-dvd1"),
        Type:                 models.Type26Enum_PUBLIC,
    }

}
```



