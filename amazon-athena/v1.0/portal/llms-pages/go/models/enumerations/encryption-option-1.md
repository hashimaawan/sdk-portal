# Encryption Option 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkVuY3J5cHRpb25PcHRpb24x

<p>Indicates whether Amazon S3 server-side encryption with Amazon S3-managed keys (<code>SSE_S3</code>), server-side encryption with KMS-managed keys (<code>SSE_KMS</code>), or client-side encryption with KMS-managed keys (<code>CSE_KMS</code>) is used.</p> <p>If a query runs in a workgroup and the workgroup overrides client-side settings, then the workgroup's setting for encryption is used. It specifies whether query results must be encrypted, for all queries that run in this workgroup. </p>



# Class Name

`EncryptionOption1Enum`


# Fields

| Name |
|  --- |
| `SSES3` |
| `SSEKMS` |
| `CSEKMS` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    encryptionOption1 := models.EncryptionOption1Enum_CSEKMS

}
```



