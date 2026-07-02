# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `encryption_option` | [`EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/encryption-option-1.md) | Required | - |
| `kms_key` | `str` | Optional | - |


# Example

```python
from amazonathena.models.encryption_configuration import EncryptionConfiguration
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum

encryption_configuration = EncryptionConfiguration(
    encryption_option=EncryptionOption1Enum.SSE_KMS,
    kms_key='KmsKey4'
)
```



