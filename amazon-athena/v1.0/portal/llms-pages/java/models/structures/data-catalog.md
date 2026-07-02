# Data Catalog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9n

<p>Contains information about a data catalog in an Amazon Web Services account.</p> <note> <p>In the Athena console, data catalogs are listed as "data sources" on the <b>Data sources</b> page under the <b>Data source name</b> column.</p> </note>
*This model accepts additional fields of type Object.*


# Class Name

`DataCatalog`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getName() | setName(String name) |
| `Description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getDescription() | setDescription(String description) |
| `Type` | [`DataCatalogType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/data-catalog-type-1.md) | Required | - | DataCatalogType1 getType() | setType(DataCatalogType1 type) |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/parameters.md) | Optional | - | Parameters getParameters() | setParameters(Parameters parameters) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.DataCatalog;
import com.amazonaws.useast1.athena.models.DataCatalogType1;
import com.amazonaws.useast1.athena.models.Parameters;
import java.io.IOException;

DataCatalog dataCatalog = new DataCatalog.Builder(
    "Name6",
    DataCatalogType1.GLUE
)
.description("Description0")
.parameters(new Parameters.Builder()
    .additionalProperty("exampleAdditionalProperty", "Parameters_additionalProperties2")
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



