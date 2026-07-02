# Result Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24x


# Class Name

`ResultConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OutputLocation` | `String` | Optional | - | String getOutputLocation() | setOutputLocation(String outputLocation) |
| `EncryptionConfiguration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/encryption-configuration-2.md) | Optional | - | EncryptionConfiguration2 getEncryptionConfiguration() | setEncryptionConfiguration(EncryptionConfiguration2 encryptionConfiguration) |
| `ExpectedBucketOwner` | `String` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` | String getExpectedBucketOwner() | setExpectedBucketOwner(String expectedBucketOwner) |
| `AclConfiguration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/acl-configuration-1.md) | Optional | - | AclConfiguration1 getAclConfiguration() | setAclConfiguration(AclConfiguration1 aclConfiguration) |


# Example

```java
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;

ResultConfiguration1 resultConfiguration1 = new ResultConfiguration1.Builder()
    .outputLocation("OutputLocation4")
    .encryptionConfiguration(new EncryptionConfiguration2.Builder(
        EncryptionOption1Enum.SSE_S3
    )
    .kmsKey("KmsKey6")
    .build())
    .expectedBucketOwner("ExpectedBucketOwner4")
    .aclConfiguration(new AclConfiguration1.Builder(
        S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL
    )
    .build())
    .build();
```



