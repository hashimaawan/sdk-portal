# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Database` | [`Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/database-2.md) | Optional | - | Database2 getDatabase() | setDatabase(Database2 database) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Database2;
import com.amazonaws.useast1.athena.models.GetDatabaseOutput;
import com.amazonaws.useast1.athena.models.Parameters;
import java.io.IOException;

GetDatabaseOutput getDatabaseOutput = new GetDatabaseOutput.Builder()
    .database(new Database2.Builder(
        "Name2"
    )
    .description("Description8")
    .parameters(new Parameters.Builder()
        .additionalProperty("exampleAdditionalProperty", "Parameters_additionalProperties2")
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



