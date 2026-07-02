# Result Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVz

The information about the updates in the query results, such as output location and encryption configuration for the query results.

*This model accepts additional fields of type interface{}.*


# Class Name

`ResultConfigurationUpdates`


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
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    resultConfigurationUpdates := models.ResultConfigurationUpdates{
        OutputLocation:                models.ToPointer("OutputLocation6"),
        RemoveOutputLocation:          models.ToPointer(false),
        EncryptionConfiguration:       models.ToPointer(models.EncryptionConfiguration2{
            EncryptionOption:      models.EncryptionOption1_SseS3,
            KmsKey:                models.ToPointer("KmsKey6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        RemoveEncryptionConfiguration: models.ToPointer(false),
        ExpectedBucketOwner:           models.ToPointer("ExpectedBucketOwner6"),
        AdditionalProperties:          map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



