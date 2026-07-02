# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |
| `Type` | [`DataCatalogType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/data-catalog-type-1.md) | Required | - | DataCatalogType1 getType() | setType(DataCatalogType1 type) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/parameters.md) | Optional | - | Parameters getParameters() | setParameters(Parameters parameters) |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/tag.md) | Optional | - | List<Tag> getTags() | setTags(List<Tag> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.CreateDataCatalogInput;
import com.amazonaws.useast1.athena.models.DataCatalogType1;
import com.amazonaws.useast1.athena.models.Parameters;
import com.amazonaws.useast1.athena.models.Tag;
import java.io.IOException;
import java.util.Arrays;

CreateDataCatalogInput createDataCatalogInput = new CreateDataCatalogInput.Builder(
    "Name6",
    DataCatalogType1.GLUE
)
.description("Description2")
.parameters(new Parameters.Builder()
    .additionalProperty("exampleAdditionalProperty", "Parameters_additionalProperties2")
        .build())
.tags(Arrays.asList(
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



