# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DatabaseList` | [`List<Database>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/database.md) | Optional | - | List<Database> getDatabaseList() | setDatabaseList(List<Database> databaseList) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.Database;
import com.amazonaws.useast1.athena.models.ListDatabasesOutput;
import com.amazonaws.useast1.athena.models.Parameters;
import java.util.Arrays;

ListDatabasesOutput listDatabasesOutput = new ListDatabasesOutput.Builder()
    .databaseList(Arrays.asList(
        new Database.Builder(
            "Name4"
        )
        .description("Description8")
        .parameters(new Parameters.Builder()
                .build())
        .build(),
        new Database.Builder(
            "Name4"
        )
        .description("Description8")
        .parameters(new Parameters.Builder()
                .build())
        .build(),
        new Database.Builder(
            "Name4"
        )
        .description("Description8")
        .parameters(new Parameters.Builder()
                .build())
        .build()
    ))
    .nextToken("NextToken6")
    .build();
```



