# Session Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9uMg

*This model accepts additional fields of type Any.*


# Class Name

`SessionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `execution_role` | `str` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `working_directory` | `str` | Optional | - |
| `idle_timeout_seconds` | `int` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.encryption_configuration import EncryptionConfiguration
from amazonathena.models.encryption_option_1 import EncryptionOption1
from amazonathena.models.session_configuration_2 import SessionConfiguration2

session_configuration_2 = SessionConfiguration2(
    execution_role='ExecutionRole2',
    working_directory='WorkingDirectory6',
    idle_timeout_seconds=142,
    encryption_configuration=EncryptionConfiguration(
        encryption_option=EncryptionOption1.SSE_S3,
        kms_key='KmsKey6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



