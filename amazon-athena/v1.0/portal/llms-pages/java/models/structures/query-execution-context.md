# Query Execution Context

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dA

The database and data catalog context in which the query execution occurs.

*This model accepts additional fields of type Object.*


# Class Name

`QueryExecutionContext`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Database` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | String getDatabase() | setDatabase(String database) |
| `Catalog` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getCatalog() | setCatalog(String catalog) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.QueryExecutionContext;
import java.io.IOException;

QueryExecutionContext queryExecutionContext = new QueryExecutionContext.Builder()
    .database("Database0")
    .catalog("Catalog6")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



