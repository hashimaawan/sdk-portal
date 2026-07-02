# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecution` | [`QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-execution-1.md) | Optional | - | QueryExecution1 getQueryExecution() | setQueryExecution(QueryExecution1 queryExecution) |


# Example

```java
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.GetQueryExecutionOutput;
import com.amazonaws.useast1.athena.models.QueryExecution1;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration2;
import com.amazonaws.useast1.athena.models.ResultReuseConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;
import com.amazonaws.useast1.athena.models.StatementType1Enum;

GetQueryExecutionOutput getQueryExecutionOutput = new GetQueryExecutionOutput.Builder()
    .queryExecution(new QueryExecution1.Builder()
        .queryExecutionId("QueryExecutionId0")
        .query("Query6")
        .statementType(StatementType1Enum.DDL)
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
        .build())
    .build();
```



