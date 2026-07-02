# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFiYXNl

Contains metadata information for a database in a data catalog.

*This model accepts additional fields of type Object.*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | String getName() | setName(String name) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/parameters.md) | Optional | - | Parameters getParameters() | setParameters(Parameters parameters) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.Database;
import com.amazonaws.useast1.athena.models.Parameters;
import java.io.IOException;

Database database = new Database.Builder(
    "Name0"
)
.description("Description6")
.parameters(new Parameters.Builder()
    .additionalProperty("exampleAdditionalProperty", "Parameters_additionalProperties2")
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



