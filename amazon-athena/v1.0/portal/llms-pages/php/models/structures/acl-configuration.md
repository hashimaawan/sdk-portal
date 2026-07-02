# Acl Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24

Indicates that an Amazon S3 canned ACL should be set to control ownership of stored query results. When Athena stores query results in Amazon S3, the canned ACL is set with the <code>x-amz-acl</code> request header. For more information about S3 Object Ownership, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html#object-ownership-overview">Object Ownership settings</a> in the <i>Amazon S3 User Guide</i>.


# Class Name

`AclConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `s3AclOption` | [`string(S3AclOption1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/s3-acl-option-1.md) | Required | - | getS3AclOption(): string | setS3AclOption(string s3AclOption): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\AclConfigurationBuilder;
use AmazonAthenaLib\Models\S3AclOption1Enum;

$aclConfiguration = AclConfigurationBuilder::init(
    S3AclOption1Enum::BUCKET_OWNER_FULL_CONTROL
)->build();
```



