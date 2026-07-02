# Database 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFiYXNlMg

*This model accepts additional fields of type Object.*


# Class Name

`Database2`


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
import com.amazonaws.useast1.athena.models.Database2;
import com.amazonaws.useast1.athena.models.Parameters;
import java.io.IOException;

Database2 database2 = new Database2.Builder(
    "Name4"
)
.description("Description2")
.parameters(new Parameters.Builder()
    .additionalProperty("exampleAdditionalProperty", "Parameters_additionalProperties2")
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



