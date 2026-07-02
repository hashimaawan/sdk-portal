# Get Database Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldERhdGFiYXNlSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetDatabaseInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CatalogName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getCatalogName() | setCatalogName(String catalogName) |
| `DatabaseName` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getDatabaseName() | setDatabaseName(String databaseName) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.GetDatabaseInput;
import java.io.IOException;

GetDatabaseInput getDatabaseInput = new GetDatabaseInput.Builder(
    "CatalogName2",
    "DatabaseName2"
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



