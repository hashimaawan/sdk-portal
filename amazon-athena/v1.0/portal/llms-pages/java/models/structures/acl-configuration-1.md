# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `S3AclOption` | [`S3AclOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/s3-acl-option-1.md) | Required | - | S3AclOption1Enum getS3AclOption() | setS3AclOption(S3AclOption1Enum s3AclOption) |


# Example

```java
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;

AclConfiguration1 aclConfiguration1 = new AclConfiguration1.Builder(
    S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL
)
.build();
```



