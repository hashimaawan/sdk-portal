# Result Configuration Updates 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVzMg


# Class Name

`ResultConfigurationUpdates2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `OutputLocation` | `*string` | Optional | - |
| `RemoveOutputLocation` | `*bool` | Optional | - |
| `EncryptionConfiguration` | [`*models.EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/encryption-configuration-2.md) | Optional | - |
| `RemoveEncryptionConfiguration` | `*bool` | Optional | - |
| `ExpectedBucketOwner` | `*string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `RemoveExpectedBucketOwner` | `*bool` | Optional | - |
| `AclConfiguration` | [`*models.AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/acl-configuration-1.md) | Optional | - |
| `RemoveAclConfiguration` | `*bool` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    resultConfigurationUpdates2 := models.ResultConfigurationUpdates2{
        OutputLocation:                models.ToPointer("OutputLocation4"),
        RemoveOutputLocation:          models.ToPointer(false),
        EncryptionConfiguration:       models.ToPointer(models.EncryptionConfiguration2{
            EncryptionOption:     models.EncryptionOption1Enum_SSES3,
            KmsKey:               models.ToPointer("KmsKey6"),
        }),
        RemoveEncryptionConfiguration: models.ToPointer(false),
        ExpectedBucketOwner:           models.ToPointer("ExpectedBucketOwner4"),
    }

}
```



