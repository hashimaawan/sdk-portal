# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type interface{}.*


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `S3AclOption` | [`models.S3AclOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/s3-acl-option-1.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    aclConfiguration1 := models.AclConfiguration1{
        S3AclOption:           models.S3AclOption1_BucketOwnerFullControl,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



