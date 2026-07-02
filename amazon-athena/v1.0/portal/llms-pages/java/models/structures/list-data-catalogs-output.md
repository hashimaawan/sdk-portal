# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DataCatalogsSummary` | [`List<DataCatalogSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/structures/data-catalog-summary.md) | Optional | - | List<DataCatalogSummary> getDataCatalogsSummary() | setDataCatalogsSummary(List<DataCatalogSummary> dataCatalogsSummary) |
| `NextToken` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | String getNextToken() | setNextToken(String nextToken) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.DataCatalogSummary;
import com.amazonaws.useast1.athena.models.DataCatalogType2;
import com.amazonaws.useast1.athena.models.ListDataCatalogsOutput;
import java.io.IOException;
import java.util.Arrays;

ListDataCatalogsOutput listDataCatalogsOutput = new ListDataCatalogsOutput.Builder()
    .dataCatalogsSummary(Arrays.asList(
        new DataCatalogSummary.Builder()
            .catalogName("CatalogName4")
            .type(DataCatalogType2.HIVE)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new DataCatalogSummary.Builder()
            .catalogName("CatalogName4")
            .type(DataCatalogType2.HIVE)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new DataCatalogSummary.Builder()
            .catalogName("CatalogName4")
            .type(DataCatalogType2.HIVE)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .nextToken("NextToken0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



