# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutions` | [`List<QueryExecution>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-execution.md) | Optional | - | List<QueryExecution> getQueryExecutions() | setQueryExecutions(List<QueryExecution> queryExecutions) |
| `UnprocessedQueryExecutionIds` | [`List<UnprocessedQueryExecutionId>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/unprocessed-query-execution-id.md) | Optional | - | List<UnprocessedQueryExecutionId> getUnprocessedQueryExecutionIds() | setUnprocessedQueryExecutionIds(List<UnprocessedQueryExecutionId> unprocessedQueryExecutionIds) |


# Example

```java
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.BatchGetQueryExecutionOutput;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.QueryExecution;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration2;
import com.amazonaws.useast1.athena.models.ResultReuseConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;
import com.amazonaws.useast1.athena.models.StatementType1Enum;
import com.amazonaws.useast1.athena.models.UnprocessedQueryExecutionId;
import java.util.Arrays;

BatchGetQueryExecutionOutput batchGetQueryExecutionOutput = new BatchGetQueryExecutionOutput.Builder()
    .queryExecutions(Arrays.asList(
        new QueryExecution.Builder()
            .queryExecutionId("QueryExecutionId6")
            .query("Query0")
            .statementType(StatementType1Enum.UTILITY)
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
            .resultReuseConfiguration(new ResultReuseConfiguration1.Builder()
                .resultReuseByAgeConfiguration(new ResultReuseByAgeConfiguration2.Builder(
                    false
                )
                .maxAgeInMinutes(26)
                .build())
                .build())
            .build(),
        new QueryExecution.Builder()
            .queryExecutionId("QueryExecutionId6")
            .query("Query0")
            .statementType(StatementType1Enum.UTILITY)
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
            .resultReuseConfiguration(new ResultReuseConfiguration1.Builder()
                .resultReuseByAgeConfiguration(new ResultReuseByAgeConfiguration2.Builder(
                    false
                )
                .maxAgeInMinutes(26)
                .build())
                .build())
            .build()
    ))
    .unprocessedQueryExecutionIds(Arrays.asList(
        new UnprocessedQueryExecutionId.Builder()
            .queryExecutionId("QueryExecutionId6")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
            .build(),
        new UnprocessedQueryExecutionId.Builder()
            .queryExecutionId("QueryExecutionId6")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
            .build(),
        new UnprocessedQueryExecutionId.Builder()
            .queryExecutionId("QueryExecutionId6")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
            .build()
    ))
    .build();
```



