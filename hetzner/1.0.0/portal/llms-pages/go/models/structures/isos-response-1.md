# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Iso` | [`models.Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/iso.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    isosResponse1 := models.IsosResponse1{
        Iso:                  models.Iso{
            Deprecated:           models.ToPointer("2018-02-28T00:00:00+00:00"),
            Description:          "FreeBSD 11.0 x64",
            Id:                   42,
            Name:                 models.ToPointer("FreeBSD-11.0-RELEASE-amd64-dvd1"),
            Type:                 models.Type26Enum_PUBLIC,
        },
    }

}
```



