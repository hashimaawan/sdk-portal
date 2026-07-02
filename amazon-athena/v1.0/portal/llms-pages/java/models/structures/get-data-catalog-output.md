# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DataCatalog` | [`DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/data-catalog-2.md) | Optional | - | DataCatalog2 getDataCatalog() | setDataCatalog(DataCatalog2 dataCatalog) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.DataCatalog2;
import com.amazonaws.useast1.athena.models.DataCatalogType1;
import com.amazonaws.useast1.athena.models.GetDataCatalogOutput;
import com.amazonaws.useast1.athena.models.Parameters;
import java.io.IOException;

GetDataCatalogOutput getDataCatalogOutput = new GetDataCatalogOutput.Builder()
    .dataCatalog(new DataCatalog2.Builder(
        "Name4",
        DataCatalogType1.GLUE
    )
    .description("Description2")
    .parameters(new Parameters.Builder()
        .additionalProperty("exampleAdditionalProperty", "Parameters_additionalProperties2")
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



