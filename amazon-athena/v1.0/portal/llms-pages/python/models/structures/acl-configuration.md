# Acl Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24

Indicates that an Amazon S3 canned ACL should be set to control ownership of stored query results. When Athena stores query results in Amazon S3, the canned ACL is set with the <code>x-amz-acl</code> request header. For more information about S3 Object Ownership, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html#object-ownership-overview">Object Ownership settings</a> in the <i>Amazon S3 User Guide</i>.

*This model accepts additional fields of type Any.*


# Class Name

`AclConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s_3_acl_option` | [`S3AclOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/s3-acl-option-1.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.acl_configuration import AclConfiguration
from amazonathena.models.s_3_acl_option_1 import S3AclOption1

acl_configuration = AclConfiguration(
    s_3_acl_option=S3AclOption1.BUCKET_OWNER_FULL_CONTROL,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



