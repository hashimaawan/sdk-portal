# Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9u

Information about a single instance of a query execution.


# Class Name

`QueryExecution`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryExecutionId` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | String getQueryExecutionId() | setQueryExecutionId(String queryExecutionId) |
| `Query` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | String getQuery() | setQuery(String query) |
| `StatementType` | [`StatementType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/statement-type-1.md) | Optional | - | StatementType1Enum getStatementType() | setStatementType(StatementType1Enum statementType) |
| `ResultConfiguration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-configuration-1.md) | Optional | - | ResultConfiguration1 getResultConfiguration() | setResultConfiguration(ResultConfiguration1 resultConfiguration) |
| `ResultReuseConfiguration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-reuse-configuration-1.md) | Optional | - | ResultReuseConfiguration1 getResultReuseConfiguration() | setResultReuseConfiguration(ResultReuseConfiguration1 resultReuseConfiguration) |
| `QueryExecutionContext` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-execution-context-1.md) | Optional | - | QueryExecutionContext1 getQueryExecutionContext() | setQueryExecutionContext(QueryExecutionContext1 queryExecutionContext) |
| `Status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/status.md) | Optional | - | Status getStatus() | setStatus(Status status) |
| `Statistics` | [`Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/statistics.md) | Optional | - | Statistics getStatistics() | setStatistics(Statistics statistics) |
| `WorkGroup` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `EngineVersion` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/engine-version-1.md) | Optional | - | EngineVersion1 getEngineVersion() | setEngineVersion(EngineVersion1 engineVersion) |
| `ExecutionParameters` | `List<String>` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` | List<String> getExecutionParameters() | setExecutionParameters(List<String> executionParameters) |
| `SubstatementType` | `String` | Optional | - | String getSubstatementType() | setSubstatementType(String substatementType) |


# Example

```java
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.QueryExecution;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.ResultReuseByAgeConfiguration2;
import com.amazonaws.useast1.athena.models.ResultReuseConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;
import com.amazonaws.useast1.athena.models.StatementType1Enum;

QueryExecution queryExecution = new QueryExecution.Builder()
    .queryExecutionId("QueryExecutionId4")
    .query("Query2")
    .statementType(StatementType1Enum.DML)
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
    .build();
```



