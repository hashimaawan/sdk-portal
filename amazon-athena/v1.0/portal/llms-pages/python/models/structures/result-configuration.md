# Result Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24

The location in Amazon S3 where query and calculation results are stored and the encryption option, if any, used for query and calculation results. These are known as "client-side settings". If workgroup settings override client-side settings, then the query uses the workgroup settings.

*This model accepts additional fields of type Any.*


# Class Name

`ResultConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `output_location` | `str` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/encryption-configuration-2.md) | Optional | - |
| `expected_bucket_owner` | `str` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `acl_configuration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/acl-configuration-1.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.result_configuration import ResultConfiguration
from amazonathena.models.s_3_acl_option_1 import S3AclOption1

result_configuration = ResultConfiguration(
    output_location='OutputLocation8',
    encryption_configuration=EncryptionConfiguration2(
        encryption_option=EncryptionOption1.SSE_S3,
        kms_key='KmsKey6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    expected_bucket_owner='ExpectedBucketOwner8',
    acl_configuration=AclConfiguration1(
        s_3_acl_option=S3AclOption1.BUCKET_OWNER_FULL_CONTROL,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



