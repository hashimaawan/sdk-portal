# Result Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24

The location in Amazon S3 where query and calculation results are stored and the encryption option, if any, used for query and calculation results. These are known as "client-side settings". If workgroup settings override client-side settings, then the query uses the workgroup settings.


# Class Name

`ResultConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `OutputLocation` | `*string` | Optional | - |
| `EncryptionConfiguration` | [`*models.EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/encryption-configuration-2.md) | Optional | - |
| `ExpectedBucketOwner` | `*string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `AclConfiguration` | [`*models.AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/acl-configuration-1.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    resultConfiguration := models.ResultConfiguration{
        OutputLocation:          models.ToPointer("OutputLocation4"),
        EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration2{
            EncryptionOption:     models.EncryptionOption1Enum_SSES3,
            KmsKey:               models.ToPointer("KmsKey6"),
        }),
        ExpectedBucketOwner:     models.ToPointer("ExpectedBucketOwner4"),
        AclConfiguration:        models.ToPointer(models.AclConfiguration1{
            S3AclOption:          models.S3AclOption1Enum_BUCKETOWNERFULLCONTROL,
        }),
    }

}
```



