# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `WorkGroup` | [`WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/work-group-2.md) | Optional | - | WorkGroup2 getWorkGroup() | setWorkGroup(WorkGroup2 workGroup) |


# Example

```java
import com.amazonaws.useast1.athena.DateTimeHelper;
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.Configuration;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.GetWorkGroupOutput;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;
import com.amazonaws.useast1.athena.models.WorkGroup2;
import com.amazonaws.useast1.athena.models.WorkGroupState3Enum;

GetWorkGroupOutput getWorkGroupOutput = new GetWorkGroupOutput.Builder()
    .workGroup(new WorkGroup2.Builder(
        "Name2"
    )
    .state(WorkGroupState3Enum.ENABLED)
    .configuration(new Configuration.Builder()
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
            .build())
    .description("Description4")
    .creationTime(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .build())
    .build();
```



