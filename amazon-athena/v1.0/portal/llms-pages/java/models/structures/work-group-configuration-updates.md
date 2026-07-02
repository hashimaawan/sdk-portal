# Work Group Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb25VcGRhdGVz

The configuration information that will be updated for this workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query results, whether the Amazon CloudWatch Metrics are enabled for the workgroup, whether the workgroup settings override the client-side settings, and the data usage limit for the amount of bytes scanned per query, if it is specified.


# Class Name

`WorkGroupConfigurationUpdates`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EnforceWorkGroupConfiguration` | `Boolean` | Optional | - | Boolean getEnforceWorkGroupConfiguration() | setEnforceWorkGroupConfiguration(Boolean enforceWorkGroupConfiguration) |
| `ResultConfigurationUpdates` | [`ResultConfigurationUpdates2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-configuration-updates-2.md) | Optional | - | ResultConfigurationUpdates2 getResultConfigurationUpdates() | setResultConfigurationUpdates(ResultConfigurationUpdates2 resultConfigurationUpdates) |
| `PublishCloudWatchMetricsEnabled` | `Boolean` | Optional | - | Boolean getPublishCloudWatchMetricsEnabled() | setPublishCloudWatchMetricsEnabled(Boolean publishCloudWatchMetricsEnabled) |
| `BytesScannedCutoffPerQuery` | `Integer` | Optional | **Constraints**: `>= 10000000` | Integer getBytesScannedCutoffPerQuery() | setBytesScannedCutoffPerQuery(Integer bytesScannedCutoffPerQuery) |
| `RemoveBytesScannedCutoffPerQuery` | `Boolean` | Optional | - | Boolean getRemoveBytesScannedCutoffPerQuery() | setRemoveBytesScannedCutoffPerQuery(Boolean removeBytesScannedCutoffPerQuery) |
| `RequesterPaysEnabled` | `Boolean` | Optional | - | Boolean getRequesterPaysEnabled() | setRequesterPaysEnabled(Boolean requesterPaysEnabled) |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-version-1.md) | Optional | - | EngineVersion1 getEngineVersion() | setEngineVersion(EngineVersion1 engineVersion) |
| `RemoveCustomerContentEncryptionConfiguration` | `Boolean` | Optional | - | Boolean getRemoveCustomerContentEncryptionConfiguration() | setRemoveCustomerContentEncryptionConfiguration(Boolean removeCustomerContentEncryptionConfiguration) |
| `AdditionalConfiguration` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getAdditionalConfiguration() | setAdditionalConfiguration(String additionalConfiguration) |
| `ExecutionRole` | `String` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | String getExecutionRole() | setExecutionRole(String executionRole) |
| `CustomerContentEncryptionConfiguration` | [`CustomerContentEncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/customer-content-encryption-configuration.md) | Optional | Specifies the KMS key that is used to encrypt the user's data stores in Athena. | CustomerContentEncryptionConfiguration getCustomerContentEncryptionConfiguration() | setCustomerContentEncryptionConfiguration(CustomerContentEncryptionConfiguration customerContentEncryptionConfiguration) |
| `EnableMinimumEncryptionConfiguration` | `Boolean` | Optional | - | Boolean getEnableMinimumEncryptionConfiguration() | setEnableMinimumEncryptionConfiguration(Boolean enableMinimumEncryptionConfiguration) |


# Example

```java
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.ResultConfigurationUpdates2;
import com.amazonaws.useast1.athena.models.WorkGroupConfigurationUpdates;

WorkGroupConfigurationUpdates workGroupConfigurationUpdates = new WorkGroupConfigurationUpdates.Builder()
    .enforceWorkGroupConfiguration(false)
    .resultConfigurationUpdates(new ResultConfigurationUpdates2.Builder()
        .outputLocation("OutputLocation0")
        .removeOutputLocation(false)
        .encryptionConfiguration(new EncryptionConfiguration2.Builder(
            EncryptionOption1Enum.SSE_S3
        )
        .kmsKey("KmsKey6")
        .build())
        .removeEncryptionConfiguration(false)
        .expectedBucketOwner("ExpectedBucketOwner0")
        .build())
    .publishCloudWatchMetricsEnabled(false)
    .bytesScannedCutoffPerQuery(10000000)
    .removeBytesScannedCutoffPerQuery(false)
    .build();
```



