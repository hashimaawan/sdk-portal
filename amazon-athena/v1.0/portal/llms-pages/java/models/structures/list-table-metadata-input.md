# List Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhSW5wdXQ


# Class Name

`ListTableMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CatalogName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getCatalogName() | setCatalogName(String catalogName) |
| `DatabaseName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getDatabaseName() | setDatabaseName(String databaseName) |
| `Expression` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` | String getExpression() | setExpression(String expression) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `MaxResults` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 50` | Integer getMaxResults() | setMaxResults(Integer maxResults) |


# Example

```java
import com.amazonaws.useast1.athena.models.ListTableMetadataInput;

ListTableMetadataInput listTableMetadataInput = new ListTableMetadataInput.Builder(
    "CatalogName2",
    "DatabaseName2"
)
.expression("Expression0")
.nextToken("NextToken8")
.maxResults(50)
.build();
```



