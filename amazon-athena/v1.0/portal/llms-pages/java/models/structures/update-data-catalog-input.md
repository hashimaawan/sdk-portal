# Update Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRlVwZGF0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`UpdateDataCatalogInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |
| `Type` | [`DataCatalogType3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/data-catalog-type-3.md) | Required | - | DataCatalogType3Enum getType() | setType(DataCatalogType3Enum type) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/parameters.md) | Optional | - | Parameters getParameters() | setParameters(Parameters parameters) |


# Example

```java
import com.amazonaws.useast1.athena.models.DataCatalogType3Enum;
import com.amazonaws.useast1.athena.models.Parameters;
import com.amazonaws.useast1.athena.models.UpdateDataCatalogInput;

UpdateDataCatalogInput updateDataCatalogInput = new UpdateDataCatalogInput.Builder(
    "Name4",
    DataCatalogType3Enum.GLUE
)
.description("Description2")
.parameters(new Parameters.Builder()
        .build())
.build();
```



