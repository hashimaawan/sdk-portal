# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutions` | [`List<QueryExecution>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-execution.md) | Optional | - | List<QueryExecution> getQueryExecutions() | setQueryExecutions(List<QueryExecution> queryExecutions) |
| `UnprocessedQueryExecutionIds` | [`List<UnprocessedQueryExecutionId>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/unprocessed-query-execution-id.md) | Optional | - | List<UnprocessedQueryExecutionId> getUnprocessedQueryExecutionIds() | setUnprocessedQueryExecutionIds(List<UnprocessedQueryExecutionId> unprocessedQueryExecutionIds) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.BatchGetQueryExecutionOutput;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1;
import com.amazonaws.useast1.athena.models.QueryExecution;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration2;
import com.amazonaws.useast1.athena.models.ResultReuseConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1;
import com.amazonaws.useast1.athena.models.StatementType1;
import com.amazonaws.useast1.athena.models.UnprocessedQueryExecutionId;
import java.io.IOException;
import java.util.Arrays;

BatchGetQueryExecutionOutput batchGetQueryExecutionOutput = new BatchGetQueryExecutionOutput.Builder()
    .queryExecutions(Arrays.asList(
        new QueryExecution.Builder()
            .queryExecutionId("QueryExecutionId6")
            .query("Query0")
            .statementType(StatementType1.UTILITY)
            .resultConfiguration(new ResultConfiguration1.Builder()
                .outputLocation("OutputLocation0")
                .encryptionConfiguration(new EncryptionConfiguration2.Builder(
                    EncryptionOption1.SSE_S3
                )
                .kmsKey("KmsKey6")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
                .expectedBucketOwner("ExpectedBucketOwner0")
                .aclConfiguration(new AclConfiguration1.Builder(
                    S3AclOption1.BUCKET_OWNER_FULL_CONTROL
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .resultReuseConfiguration(new ResultReuseConfiguration1.Builder()
                .resultReuseByAgeConfiguration(new ResultReuseByAgeConfiguration2.Builder(
                    false
                )
                .maxAgeInMinutes(26)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new QueryExecution.Builder()
            .queryExecutionId("QueryExecutionId6")
            .query("Query0")
            .statementType(StatementType1.UTILITY)
            .resultConfiguration(new ResultConfiguration1.Builder()
                .outputLocation("OutputLocation0")
                .encryptionConfiguration(new EncryptionConfiguration2.Builder(
                    EncryptionOption1.SSE_S3
                )
                .kmsKey("KmsKey6")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
                .expectedBucketOwner("ExpectedBucketOwner0")
                .aclConfiguration(new AclConfiguration1.Builder(
                    S3AclOption1.BUCKET_OWNER_FULL_CONTROL
                )
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .resultReuseConfiguration(new ResultReuseConfiguration1.Builder()
                .resultReuseByAgeConfiguration(new ResultReuseByAgeConfiguration2.Builder(
                    false
                )
                .maxAgeInMinutes(26)
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .unprocessedQueryExecutionIds(Arrays.asList(
        new UnprocessedQueryExecutionId.Builder()
            .queryExecutionId("QueryExecutionId6")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new UnprocessedQueryExecutionId.Builder()
            .queryExecutionId("QueryExecutionId6")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new UnprocessedQueryExecutionId.Builder()
            .queryExecutionId("QueryExecutionId6")
            .errorCode("ErrorCode2")
            .errorMessage("ErrorMessage8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



