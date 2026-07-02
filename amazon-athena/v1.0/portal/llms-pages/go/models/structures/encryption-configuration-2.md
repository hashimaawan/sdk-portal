# Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9uMg


# Class Name

`EncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EncryptionOption` | [`models.EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/enumerations/encryption-option-1.md) | Required | - |
| `KmsKey` | `*string` | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    encryptionConfiguration2 := models.EncryptionConfiguration2{
        EncryptionOption:     models.EncryptionOption1Enum_SSES3,
        KmsKey:               models.ToPointer("KmsKey2"),
    }

}
```



