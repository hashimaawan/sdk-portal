# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x


# Class Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `S3AclOption` | [`S3AclOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/s3-acl-option-1.md) | Required | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

AclConfiguration1 aclConfiguration1 = new AclConfiguration1
{
    S3AclOption = S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
};
```



