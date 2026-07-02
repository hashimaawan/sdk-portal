# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DataCatalog` | [`DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/data-catalog-2.md) | Optional | - | DataCatalog2 getDataCatalog() | setDataCatalog(DataCatalog2 dataCatalog) |


# Example

```java
import com.amazonaws.useast1.athena.models.DataCatalog2;
import com.amazonaws.useast1.athena.models.DataCatalogType1Enum;
import com.amazonaws.useast1.athena.models.GetDataCatalogOutput;
import com.amazonaws.useast1.athena.models.Parameters;

GetDataCatalogOutput getDataCatalogOutput = new GetDataCatalogOutput.Builder()
    .dataCatalog(new DataCatalog2.Builder(
        "Name4",
        DataCatalogType1Enum.GLUE
    )
    .description("Description2")
    .parameters(new Parameters.Builder()
            .build())
    .build())
    .build();
```



