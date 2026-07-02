# Work Group Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb24

The configuration of the workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query and calculation results, whether the Amazon CloudWatch Metrics are enabled for the workgroup and whether workgroup settings override query settings, and the data usage limits for the amount of data scanned per query or per workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.


# Class Name

`WorkGroupConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ResultConfiguration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-configuration-1.md) | Optional | - | ResultConfiguration1 getResultConfiguration() | setResultConfiguration(ResultConfiguration1 resultConfiguration) |
| `EnforceWorkGroupConfiguration` | `Boolean` | Optional | - | Boolean getEnforceWorkGroupConfiguration() | setEnforceWorkGroupConfiguration(Boolean enforceWorkGroupConfiguration) |
| `PublishCloudWatchMetricsEnabled` | `Boolean` | Optional | - | Boolean getPublishCloudWatchMetricsEnabled() | setPublishCloudWatchMetricsEnabled(Boolean publishCloudWatchMetricsEnabled) |
| `BytesScannedCutoffPerQuery` | `Integer` | Optional | **Constraints**: `>= 10000000` | Integer getBytesScannedCutoffPerQuery() | setBytesScannedCutoffPerQuery(Integer bytesScannedCutoffPerQuery) |
| `RequesterPaysEnabled` | `Boolean` | Optional | - | Boolean getRequesterPaysEnabled() | setRequesterPaysEnabled(Boolean requesterPaysEnabled) |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-version-1.md) | Optional | - | EngineVersion1 getEngineVersion() | setEngineVersion(EngineVersion1 engineVersion) |
| `AdditionalConfiguration` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getAdditionalConfiguration() | setAdditionalConfiguration(String additionalConfiguration) |
| `ExecutionRole` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | String getExecutionRole() | setExecutionRole(String executionRole) |
| `CustomerContentEncryptionConfiguration` | [`CustomerContentEncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/customer-content-encryption-configuration-2.md) | Optional | - | CustomerContentEncryptionConfiguration2 getCustomerContentEncryptionConfiguration() | setCustomerContentEncryptionConfiguration(CustomerContentEncryptionConfiguration2 customerContentEncryptionConfiguration) |
| `EnableMinimumEncryptionConfiguration` | `Boolean` | Optional | - | Boolean getEnableMinimumEncryptionConfiguration() | setEnableMinimumEncryptionConfiguration(Boolean enableMinimumEncryptionConfiguration) |


# Example

```java
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;
import com.amazonaws.useast1.athena.models.WorkGroupConfiguration;

WorkGroupConfiguration workGroupConfiguration = new WorkGroupConfiguration.Builder()
    .resultConfiguration(new ResultConfiguration1.Builder()
        .outputLocation("OutputLocation0")
        .encryptionConfiguration(new EncryptionConfiguration2.Builder(
            EncryptionOption1Enum.SSE_S3
        )
        .kmsKey("KmsKey6")
        .build())
        .expectedBucketOwner("ExpectedBucketOwner0")
        .aclConfiguration(new AclConfiguration1.Builder(
            S3AclOption1Enum.BUCKET_OWNER_FULL_CONTROL
        )
        .build())
        .build())
    .enforceWorkGroupConfiguration(false)
    .publishCloudWatchMetricsEnabled(false)
    .bytesScannedCutoffPerQuery(10000000)
    .requesterPaysEnabled(false)
    .build();
```



