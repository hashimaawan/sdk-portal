# Result Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24

The location in Amazon S3 where query and calculation results are stored and the encryption option, if any, used for query and calculation results. These are known as "client-side settings". If workgroup settings override client-side settings, then the query uses the workgroup settings.

*This model accepts additional fields of type Object.*


# Class Name

`ResultConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `OutputLocation` | `String` | Optional | - | String getOutputLocation() | setOutputLocation(String outputLocation) |
| `EncryptionConfiguration` | [`EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/encryption-configuration-2.md) | Optional | - | EncryptionConfiguration2 getEncryptionConfiguration() | setEncryptionConfiguration(EncryptionConfiguration2 encryptionConfiguration) |
| `ExpectedBucketOwner` | `String` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` | String getExpectedBucketOwner() | setExpectedBucketOwner(String expectedBucketOwner) |
| `AclConfiguration` | [`AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/acl-configuration-1.md) | Optional | - | AclConfiguration1 getAclConfiguration() | setAclConfiguration(AclConfiguration1 aclConfiguration) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.ResultConfiguration;
import com.amazonaws.useast1.athena.models.S3AclOption1;
import java.io.IOException;

ResultConfiguration resultConfiguration = new ResultConfiguration.Builder()
    .outputLocation("OutputLocation4")
    .encryptionConfiguration(new EncryptionConfiguration2.Builder(
        EncryptionOption1.SSE_S3
    )
    .kmsKey("KmsKey6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
    .expectedBucketOwner("ExpectedBucketOwner4")
    .aclConfiguration(new AclConfiguration1.Builder(
        S3AclOption1.BUCKET_OWNER_FULL_CONTROL
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



