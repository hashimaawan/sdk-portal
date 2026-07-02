# S3 Acl Option 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlMzQWNsT3B0aW9uMQ

The Amazon S3 canned ACL that Athena should specify when storing query results. Currently the only supported canned ACL is <code>BUCKET_OWNER_FULL_CONTROL</code>. If a query runs in a workgroup and the workgroup overrides client-side settings, then the Amazon S3 canned ACL specified in the workgroup's settings is used for all queries that run in the workgroup. For more information about Amazon S3 canned ACLs, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/acl-overview.html#canned-acl">Canned ACL</a> in the <i>Amazon S3 User Guide</i>.


# Enum Type Name

`S3AclOption1Enum`


# Fields

| Name |
|  --- |
| `BUCKET_OWNER_FULL_CONTROL` |


# Example

```java
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;

S3AclOption1Enum s3AclOption1 = S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL;
```



