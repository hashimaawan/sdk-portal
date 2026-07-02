# Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50SW5wdXQ


# Class Name

`GetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `StatementName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` | String getStatementName() | setStatementName(String statementName) |
| `WorkGroup` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | String getWorkGroup() | setWorkGroup(String workGroup) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetPreparedStatementInput;

GetPreparedStatementInput getPreparedStatementInput = new GetPreparedStatementInput.Builder(
    "StatementName6",
    "WorkGroup0"
)
.build();
```



