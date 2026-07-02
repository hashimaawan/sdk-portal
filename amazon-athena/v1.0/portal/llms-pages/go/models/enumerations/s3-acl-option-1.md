# S3 Acl Option 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlMzQWNsT3B0aW9uMQ

The Amazon S3 canned ACL that Athena should specify when storing query results. Currently the only supported canned ACL is <code>BUCKET_OWNER_FULL_CONTROL</code>. If a query runs in a workgroup and the workgroup overrides client-side settings, then the Amazon S3 canned ACL specified in the workgroup's settings is used for all queries that run in the workgroup. For more information about Amazon S3 canned ACLs, see <a href="https://docs.aws.amazon.com/AmazonS3/latest/userguide/acl-overview.html#canned-acl">Canned ACL</a> in the <i>Amazon S3 User Guide</i>.


# Class Name

`S3AclOption1Enum`


# Fields

| Name |
|  --- |
| `BUCKETOWNERFULLCONTROL` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    s3AclOption1 := models.S3AclOption1Enum_BUCKETOWNERFULLCONTROL

}
```



