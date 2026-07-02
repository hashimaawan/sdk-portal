# Batch Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRJbnB1dA


# Class Name

`BatchGetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PreparedStatementNames` | `List<String>` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | List<String> getPreparedStatementNames() | setPreparedStatementNames(List<String> preparedStatementNames) |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |


# Example

```java
import com.amazonaws.useast1.athena.models.BatchGetPreparedStatementInput;
import java.util.Arrays;

BatchGetPreparedStatementInput batchGetPreparedStatementInput = new BatchGetPreparedStatementInput.Builder(
    Arrays.asList(
        "PreparedStatementNames8",
        "PreparedStatementNames9",
        "PreparedStatementNames0"
    ),
    "WorkGroup6"
)
.build();
```



