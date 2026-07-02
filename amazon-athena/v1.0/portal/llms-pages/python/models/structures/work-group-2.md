# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRldvcmtHcm91cDI


# Class Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/work-group-state-3.md) | Optional | - |
| `configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/configuration.md) | Optional | - |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creation_time` | `datetime` | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.configuration import Configuration
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.s_3_acl_option_1_enum import S3AclOption1Enum
from amazonathena.models.work_group_2 import WorkGroup2
from amazonathena.models.work_group_state_3_enum import WorkGroupState3Enum

work_group_2 = WorkGroup2(
    name='Name8',
    state=WorkGroupState3Enum.ENABLED,
    configuration=Configuration(
        result_configuration=ResultConfiguration1(
            output_location='OutputLocation0',
            encryption_configuration=EncryptionConfiguration2(
                encryption_option=EncryptionOption1Enum.SSE_S3,
                kms_key='KmsKey6'
            ),
            expected_bucket_owner='ExpectedBucketOwner0',
            acl_configuration=AclConfiguration1(
                s_3_acl_option=S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL
            )
        ),
        enforce_work_group_configuration=False,
        publish_cloud_watch_metrics_enabled=False,
        bytes_scanned_cutoff_per_query=10000000,
        requester_pays_enabled=False
    ),
    description='Description4',
    creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z')
)
```



