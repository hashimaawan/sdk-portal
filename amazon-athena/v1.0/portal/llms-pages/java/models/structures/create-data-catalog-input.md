# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |
| `Type` | [`DataCatalogType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/data-catalog-type-1.md) | Required | - | DataCatalogType1Enum getType() | setType(DataCatalogType1Enum type) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/parameters.md) | Optional | - | Parameters getParameters() | setParameters(Parameters parameters) |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/tag.md) | Optional | - | List<Tag> getTags() | setTags(List<Tag> tags) |


# Example

```java
import com.amazonaws.useast1.athena.models.CreateDataCatalogInput;
import com.amazonaws.useast1.athena.models.DataCatalogType1Enum;
import com.amazonaws.useast1.athena.models.Parameters;
import com.amazonaws.useast1.athena.models.Tag;
import java.util.Arrays;

CreateDataCatalogInput createDataCatalogInput = new CreateDataCatalogInput.Builder(
    "Name6",
    DataCatalogType1Enum.GLUE
)
.description("Description2")
.parameters(new Parameters.Builder()
        .build())
.tags(Arrays.asList(
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
            .build(),
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
            .build(),
        new Tag.Builder()
            .key("Key0")
            .value("Value6")
            .build()
    ))
.build();
```



