# Result Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVz

The information about the updates in the query results, such as output location and encryption configuration for the query results.


# Class Name

`ResultConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `output_location` | `str` | Optional | - |
| `remove_output_location` | `bool` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/encryption-configuration-2.md) | Optional | - |
| `remove_encryption_configuration` | `bool` | Optional | - |
| `expected_bucket_owner` | `str` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `remove_expected_bucket_owner` | `bool` | Optional | - |
| `acl_configuration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/acl-configuration-1.md) | Optional | - |
| `remove_acl_configuration` | `bool` | Optional | - |


# Example

```python
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum
from amazonathena.models.result_configuration_updates import ResultConfigurationUpdates

result_configuration_updates = ResultConfigurationUpdates(
    output_location='OutputLocation0',
    remove_output_location=False,
    encryption_configuration=EncryptionConfiguration2(
        encryption_option=EncryptionOption1Enum.SSE_S3,
        kms_key='KmsKey6'
    ),
    remove_encryption_configuration=False,
    expected_bucket_owner='ExpectedBucketOwner0'
)
```



