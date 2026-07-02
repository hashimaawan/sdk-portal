# Result Configuration Updates 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVzMg


# Class Name

`ResultConfigurationUpdates2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OutputLocation` | `String` | Optional | - | String getOutputLocation() | setOutputLocation(String outputLocation) |
| `RemoveOutputLocation` | `Boolean` | Optional | - | Boolean getRemoveOutputLocation() | setRemoveOutputLocation(Boolean removeOutputLocation) |
| `EncryptionConfiguration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/encryption-configuration-2.md) | Optional | - | EncryptionConfiguration2 getEncryptionConfiguration() | setEncryptionConfiguration(EncryptionConfiguration2 encryptionConfiguration) |
| `RemoveEncryptionConfiguration` | `Boolean` | Optional | - | Boolean getRemoveEncryptionConfiguration() | setRemoveEncryptionConfiguration(Boolean removeEncryptionConfiguration) |
| `ExpectedBucketOwner` | `String` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` | String getExpectedBucketOwner() | setExpectedBucketOwner(String expectedBucketOwner) |
| `RemoveExpectedBucketOwner` | `Boolean` | Optional | - | Boolean getRemoveExpectedBucketOwner() | setRemoveExpectedBucketOwner(Boolean removeExpectedBucketOwner) |
| `AclConfiguration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/acl-configuration-1.md) | Optional | - | AclConfiguration1 getAclConfiguration() | setAclConfiguration(AclConfiguration1 aclConfiguration) |
| `RemoveAclConfiguration` | `Boolean` | Optional | - | Boolean getRemoveAclConfiguration() | setRemoveAclConfiguration(Boolean removeAclConfiguration) |


# Example

```java
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.ResultConfigurationUpdates2;

ResultConfigurationUpdates2 resultConfigurationUpdates2 = new ResultConfigurationUpdates2.Builder()
    .outputLocation("OutputLocation4")
    .removeOutputLocation(false)
    .encryptionConfiguration(new EncryptionConfiguration2.Builder(
        EncryptionOption1Enum.SSE_S3
    )
    .kmsKey("KmsKey6")
    .build())
    .removeEncryptionConfiguration(false)
    .expectedBucketOwner("ExpectedBucketOwner4")
    .build();
```



