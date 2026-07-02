# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type Any.*


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `configuration` | [`Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/configuration.md) | Optional | - |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `tags` | [`List[Tag]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/tag.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.configuration import Configuration
from amazonathena.models.create_work_group_input import CreateWorkGroupInput
from amazonathena.models.encryption_configuration_2 import EncryptionConfiguration2
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.result_configuration_1 import ResultConfiguration1
from amazonathena.models.s_3_acl_option_1 import S3AclOption1
from amazonathena.models.tag import Tag

create_work_group_input = CreateWorkGroupInput(
    name='Name8',
    configuration=Configuration(
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
    ),
    description='Description8',
    tags=[
        Tag(
            key='Key0',
            value='Value6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



