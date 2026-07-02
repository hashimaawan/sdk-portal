# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `S3AclOption` | [`models.S3AclOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/s3-acl-option-1.md) | Required | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    aclConfiguration1 := models.AclConfiguration1{
        S3AclOption:          models.S3AclOption1Enum_BUCKETOWNERFULLCONTROL,
    }

}
```



