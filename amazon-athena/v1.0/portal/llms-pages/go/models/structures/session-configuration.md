# Session Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9u

Contains session configuration information.

*This model accepts additional fields of type interface{}.*


# Class Name

`SessionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExecutionRole` | `*string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `WorkingDirectory` | `*string` | Optional | - |
| `IdleTimeoutSeconds` | `*int` | Optional | - |
| `EncryptionConfiguration` | [`*models.EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    sessionConfiguration := models.SessionConfiguration{
        ExecutionRole:           models.ToPointer("ExecutionRole2"),
        WorkingDirectory:        models.ToPointer("WorkingDirectory6"),
        IdleTimeoutSeconds:      models.ToPointer(188),
        EncryptionConfiguration: models.ToPointer(models.EncryptionConfiguration{
            EncryptionOption:      models.EncryptionOption1_SseS3,
            KmsKey:                models.ToPointer("KmsKey6"),
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



