# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.

*This model accepts additional fields of type Any.*


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `encryption_option` | [`EncryptionOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/encryption-option-1.md) | Required | - |
| `kms_key` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.encryption_configuration import EncryptionConfiguration
from amazonathena.models.encryption_option_1 import EncryptionOption1

encryption_configuration = EncryptionConfiguration(
    encryption_option=EncryptionOption1.SSE_KMS,
    kms_key='KmsKey4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



