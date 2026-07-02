# Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25VcGRhdGVz

*This model accepts additional fields of type Any.*


# Class Name

`ConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enforce_work_group_configuration` | `bool` | Optional | - |
| `result_configuration_updates` | [`ResultConfigurationUpdates2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result-configuration-updates-2.md) | Optional | - |
| `publish_cloud_watch_metrics_enabled` | `bool` | Optional | - |
| `bytes_scanned_cutoff_per_query` | `int` | Optional | **Constraints**: `>= 10000000` |
| `remove_bytes_scanned_cutoff_per_query` | `bool` | Optional | - |
| `requester_pays_enabled` | `bool` | Optional | - |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-version-1.md) | Optional | - |
| `remove_customer_content_encryption_configuration` | `bool` | Optional | - |
| `additional_configuration` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `execution_role` | `str` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `customer_content_encryption_configuration` | [`CustomerContentEncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/customer-content-encryption-configuration.md) | Optional | Specifies the KMS key that is used to encrypt the user's data stores in Athena. |
| `enable_minimum_encryption_configuration` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.configuration_updates import ConfigurationUpdates
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.result_configuration_updates_2 import ResultConfigurationUpdates2

configuration_updates = ConfigurationUpdates(
    enforce_work_group_configuration=False,
    result_configuration_updates=ResultConfigurationUpdates2(
        output_location='OutputLocation0',
        remove_output_location=False,
        encryption_configuration=EncryptionConfiguration2(
            encryption_option=EncryptionOption1.SSE_S3,
            kms_key='KmsKey6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        remove_encryption_configuration=False,
        expected_bucket_owner='ExpectedBucketOwner0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    publish_cloud_watch_metrics_enabled=False,
    bytes_scanned_cutoff_per_query=10000000,
    remove_bytes_scanned_cutoff_per_query=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



