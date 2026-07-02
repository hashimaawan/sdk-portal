# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0


# Class Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `configuration_updates` | [`ConfigurationUpdates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/configuration-updates.md) | Optional | - |
| `state` | [`WorkGroupState2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/work-group-state-2.md) | Optional | - |


# Example

```python
from amazonathena.models.configuration_updates import ConfigurationUpdates
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum
from amazonathena.models.result_configuration_updates_2 import ResultConfigurationUpdates2
from amazonathena.models.update_work_group_input import UpdateWorkGroupInput
from amazonathena.models.work_group_state_2_enum import WorkGroupState2Enum

update_work_group_input = UpdateWorkGroupInput(
    work_group='WorkGroup0',
    description='Description8',
    configuration_updates=ConfigurationUpdates(
        enforce_work_group_configuration=False,
        result_configuration_updates=ResultConfigurationUpdates2(
            output_location='OutputLocation0',
            remove_output_location=False,
            encryption_configuration=EncryptionConfiguration2(
                encryption_option=EncryptionOption1Enum.SSE_S3,
                kms_key='KmsKey6'
            ),
            remove_encryption_configuration=False,
            expected_bucket_owner='ExpectedBucketOwner0'
        ),
        publish_cloud_watch_metrics_enabled=False,
        bytes_scanned_cutoff_per_query=10000000,
        remove_bytes_scanned_cutoff_per_query=False
    ),
    state=WorkGroupState2Enum.ENABLED
)
```



