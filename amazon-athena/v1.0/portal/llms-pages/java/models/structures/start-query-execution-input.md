# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA


# Class Name

`StartQueryExecutionInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `QueryString` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | String getQueryString() | setQueryString(String queryString) |
| `ClientRequestToken` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | String getClientRequestToken() | setClientRequestToken(String clientRequestToken) |
| `QueryExecutionContext` | [`QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/query-execution-context-1.md) | Optional | - | QueryExecutionContext1 getQueryExecutionContext() | setQueryExecutionContext(QueryExecutionContext1 queryExecutionContext) |
| `ResultConfiguration` | [`ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-configuration-1.md) | Optional | - | ResultConfiguration1 getResultConfiguration() | setResultConfiguration(ResultConfiguration1 resultConfiguration) |
| `WorkGroup` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |
| `ExecutionParameters` | `List<String>` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` | List<String> getExecutionParameters() | setExecutionParameters(List<String> executionParameters) |
| `ResultReuseConfiguration` | [`ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/result-reuse-configuration-1.md) | Optional | - | ResultReuseConfiguration1 getResultReuseConfiguration() | setResultReuseConfiguration(ResultReuseConfiguration1 resultReuseConfiguration) |


# Example

```java
import com.amazonaws.useast1.athena.models.AclConfiguration1;
import com.amazonaws.useast1.athena.models.EncryptionConfiguration2;
import com.amazonaws.useast1.athena.models.EncryptionOption1Enum;
import com.amazonaws.useast1.athena.models.QueryExecutionContext1;
import com.amazonaws.useast1.athena.models.ResultConfiguration1;
import com.amazonaws.useast1.athena.models.S3AclOption1Enum;
import com.amazonaws.useast1.athena.models.StartQueryExecutionInput;
import java.util.Arrays;

StartQueryExecutionInput startQueryExecutionInput = new StartQueryExecutionInput.Builder(
    "QueryString4"
)
.clientRequestToken("ClientRequestToken6")
.queryExecutionContext(new QueryExecutionContext1.Builder()
        .database("Database4")
        .catalog("Catalog0")
        .build())
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
.workGroup("WorkGroup4")
.executionParameters(Arrays.asList(
        "ExecutionParameters8"
    ))
.build();
```



