# Data Catalog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9n

<p>Contains information about a data catalog in an Amazon Web Services account.</p> <note> <p>In the Athena console, data catalogs are listed as "data sources" on the <b>Data sources</b> page under the <b>Data source name</b> column.</p> </note>



# Class Name

`DataCatalog`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Type` | [`DataCatalogType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/data-catalog-type-1.md) | Required | - | DataCatalogType1Enum getType() | setType(DataCatalogType1Enum type) |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/parameters.md) | Optional | - | Parameters getParameters() | setParameters(Parameters parameters) |


# Example

```java
import com.amazonaws.useast1.athena.models.DataCatalog;
import com.amazonaws.useast1.athena.models.DataCatalogType1Enum;
import com.amazonaws.useast1.athena.models.Parameters;

DataCatalog dataCatalog = new DataCatalog.Builder(
    "Name6",
    DataCatalogType1Enum.GLUE
)
.description("Description0")
.parameters(new Parameters.Builder()
        .build())
.build();
```



