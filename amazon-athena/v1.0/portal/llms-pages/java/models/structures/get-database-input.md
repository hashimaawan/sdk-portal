# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ


# Class Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CatalogName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getCatalogName() | setCatalogName(String catalogName) |
| `DatabaseName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getDatabaseName() | setDatabaseName(String databaseName) |


# Example

```java
import com.amazonaws.useast1.athena.models.GetDatabaseInput;

GetDatabaseInput getDatabaseInput = new GetDatabaseInput.Builder(
    "CatalogName2",
    "DatabaseName2"
)
.build();
```



