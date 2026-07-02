# Acl Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkFjbENvbmZpZ3VyYXRpb24

Indicates that an Amazon S3 canned ACL should be set to control ownership of stored query results. When Athena stores query results in Amazon S3, the canned ACL is set with the <code>x-amz-acl</code> request header. For more information about S3 Object Ownership, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html#object-ownership-overview">Object Ownership settings</a> in the <i>Amazon S3 User Guide</i>.

*This model accepts additional fields of type unknown.*


# Interface Name

`AclConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s3AclOption` | [`S3AclOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/s3-acl-option-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AclConfiguration, S3AclOption1 } from 'amazon-athenalib';

const aclConfiguration: AclConfiguration = {
  s3AclOption: S3AclOption1.BucketOwnerFullControl,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



