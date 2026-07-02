# Work Group Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb24

The configuration of the workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query and calculation results, whether the Amazon CloudWatch Metrics are enabled for the workgroup and whether workgroup settings override query settings, and the data usage limits for the amount of data scanned per query or per workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.

*This model accepts additional fields of type Any.*


# Class Name

`WorkGroupConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `result_configuration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-configuration-1.md) | Optional | - |
| `enforce_work_group_configuration` | `bool` | Optional | - |
| `publish_cloud_watch_metrics_enabled` | `bool` | Optional | - |
| `bytes_scanned_cutoff_per_query` | `int` | Optional | **Constraints**: `>= 10000000` |
| `requester_pays_enabled` | `bool` | Optional | - |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-version-1.md) | Optional | - |
| `additional_configuration` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `execution_role` | `str` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `customer_content_encryption_configuration` | [`CustomerContentEncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/customer-content-encryption-configuration-2.md) | Optional | - |
| `enable_minimum_encryption_configuration` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.s_3_acl_option_1 import S3AclOption1
from amazonathena.models.work_group_configuration import WorkGroupConfiguration

work_group_configuration = WorkGroupConfiguration(
    result_configuration=ResultConfiguration1(
        output_location='OutputLocation0',
        encryption_configuration=EncryptionConfiguration2(
            encryption_option=EncryptionOption1.SSE_S3,
            kms_key='KmsKey6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        expected_bucket_owner='ExpectedBucketOwner0',
        acl_configuration=AclConfiguration1(
            s_3_acl_option=S3AclOption1.BUCKET_OWNER_FULL_CONTROL,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    enforce_work_group_configuration=False,
    publish_cloud_watch_metrics_enabled=False,
    bytes_scanned_cutoff_per_query=10000000,
    requester_pays_enabled=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



