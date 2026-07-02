# Acl Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24x


# Interface Name

`AclConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s3AclOption` | [`S3AclOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/s3-acl-option-1.md) | Required | - |


# Example

```ts
import { AclConfiguration1, S3AclOption1Enum } from 'amazon-athenalib';

const aclConfiguration1: AclConfiguration1 = {
  s3AclOption: S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
};
```



