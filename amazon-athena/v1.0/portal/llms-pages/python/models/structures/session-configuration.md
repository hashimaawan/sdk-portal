# Session Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9u

Contains session configuration information.


# Class Name

`SessionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `execution_role` | `str` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `working_directory` | `str` | Optional | - |
| `idle_timeout_seconds` | `int` | Optional | - |
| `encryption_configuration` | [`EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |


# Example

```python
from amazonathena.models.encryption_configuration import EncryptionConfiguration
from amazonathena.models.encryption_option_1_enum import EncryptionOption1Enum
from amazonathena.models.session_configuration import SessionConfiguration

session_configuration = SessionConfiguration(
    execution_role='ExecutionRole8',
    working_directory='WorkingDirectory2',
    idle_timeout_seconds=176,
    encryption_configuration=EncryptionConfiguration(
        encryption_option=EncryptionOption1Enum.SSE_S3,
        kms_key='KmsKey6'
    )
)
```



