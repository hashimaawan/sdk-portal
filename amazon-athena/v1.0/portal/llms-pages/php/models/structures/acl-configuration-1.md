# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `s3AclOption` | [`string(S3AclOption1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/s3-acl-option-1.md) | Required | - | getS3AclOption(): string | setS3AclOption(string s3AclOption): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;

$aclConfiguration1 = AclConfiguration1Builder::init(
    S3AclOption1Enum::BUCKET_OWNER_FULL_CONTROL
)->build();
```



