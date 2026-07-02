# Result Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVz

The information about the updates in the query results, such as output location and encryption configuration for the query results.

*This model accepts additional fields of type Object.*


# Class Name

`ResultConfigurationUpdates`


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
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.ResultConfigurationUpdates;
import java.io.IOException;

ResultConfigurationUpdates resultConfigurationUpdates = new ResultConfigurationUpdates.Builder()
    .outputLocation("OutputLocation6")
    .removeOutputLocation(false)
    .encryptionConfiguration(new EncryptionConfiguration2.Builder(
        EncryptionOption1.SSE_S3
    )
    .kmsKey("KmsKey6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
    .removeEncryptionConfiguration(false)
    .expectedBucketOwner("ExpectedBucketOwner6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



