# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DataCatalogsSummary` | [`List<DataCatalogSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/data-catalog-summary.md) | Optional | - | List<DataCatalogSummary> getDataCatalogsSummary() | setDataCatalogsSummary(List<DataCatalogSummary> dataCatalogsSummary) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |


# Example

```java
import com.amazonaws.useast1.athena.models.DataCatalogSummary;
import com.amazonaws.useast1.athena.models.DataCatalogType2Enum;
import com.amazonaws.useast1.athena.models.ListDataCatalogsOutput;
import java.util.Arrays;

ListDataCatalogsOutput listDataCatalogsOutput = new ListDataCatalogsOutput.Builder()
    .dataCatalogsSummary(Arrays.asList(
        new DataCatalogSummary.Builder()
            .catalogName("CatalogName4")
            .type(DataCatalogType2Enum.HIVE)
            .build(),
        new DataCatalogSummary.Builder()
            .catalogName("CatalogName4")
            .type(DataCatalogType2Enum.HIVE)
            .build(),
        new DataCatalogSummary.Builder()
            .catalogName("CatalogName4")
            .type(DataCatalogType2Enum.HIVE)
            .build()
    ))
    .nextToken("NextToken0")
    .build();
```



