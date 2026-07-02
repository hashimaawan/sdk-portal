# Result Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24x


# Class Name

`ResultConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `output_location` | `str` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/encryption-configuration-2.md) | Optional | - |
| `expected_bucket_owner` | `str` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `acl_configuration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/acl-configuration-1.md) | Optional | - |


# Example

```python
from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.s_3_acl_option_1_enum import S3AclOption1Enum

result_configuration_1 = ResultConfiguration1(
    output_location='OutputLocation2',
    encryption_configuration=EncryptionConfiguration2(
        encryption_option=EncryptionOption1Enum.SSE_S3,
        kms_key='KmsKey6'
    ),
    expected_bucket_owner='ExpectedBucketOwner2',
    acl_configuration=AclConfiguration1(
        s_3_acl_option=S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL
    )
)
```



