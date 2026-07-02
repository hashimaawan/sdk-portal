# Result Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24

The location in Amazon S3 where query and calculation results are stored and the encryption option, if any, used for query and calculation results. These are known as "client-side settings". If workgroup settings override client-side settings, then the query uses the workgroup settings.

*This model accepts additional fields of type interface{}.*


# Class Name

`ResultConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `OutputLocation` | `*string` | Optional | - |
| `EncryptionConfiguration` | [`*models.EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/encryption-configuration-2.md) | Optional | - |
| `ExpectedBucketOwner` | `*string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `AclConfiguration` | [`*models.AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/acl-configuration-1.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    resultConfiguration := models.ResultConfiguration{
        OutputLocation:          models.ToPointer("OutputLocation4"),
        EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration2{
            EncryptionOption:      models.EncryptionOption1_SseS3,
            KmsKey:                models.ToPointer("KmsKey6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        ExpectedBucketOwner:     models.ToPointer("ExpectedBucketOwner4"),
        AclConfiguration:        models.ToPointer(models.AclConfiguration1{
            S3AclOption:           models.S3AclOption1_BucketOwnerFullControl,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:    map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



