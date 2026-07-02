# Get Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFJbnB1dA


# Class Name

`GetTableMetadataInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CatalogName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getCatalogName() | setCatalogName(String catalogName) |
| `DatabaseName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getDatabaseName() | setDatabaseName(String databaseName) |
| `TableName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getTableName() | setTableName(String tableName) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetTableMetadataInput;

GetTableMetadataInput getTableMetadataInput = new GetTableMetadataInput.Builder(
    "CatalogName2",
    "DatabaseName2",
    "TableName4"
)
.build();
```



