# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s_3_acl_option` | [`S3AclOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/s3-acl-option-1.md) | Required | - |


# Example

```python
from amazonathena.models.acl_configuration_1 import AclConfiguration1
from amazonathena.models.s_3_acl_option_1_enum import S3AclOption1Enum

acl_configuration_1 = AclConfiguration1(
    s_3_acl_option=S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL
)
```



