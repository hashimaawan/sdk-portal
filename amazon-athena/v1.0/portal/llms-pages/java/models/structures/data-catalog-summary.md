# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.

*This model accepts additional fields of type Object.*


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CatalogName` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getCatalogName() | setCatalogName(String catalogName) |
| `Type` | [`DataCatalogType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/data-catalog-type-2.md) | Optional | - | DataCatalogType2 getType() | setType(DataCatalogType2 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.amazonaws.useast1.athena.ApiHelper;
import com.amazonaws.useast1.athena.models.DataCatalogSummary;
import com.amazonaws.useast1.athena.models.DataCatalogType2;
import java.io.IOException;

DataCatalogSummary dataCatalogSummary = new DataCatalogSummary.Builder()
    .catalogName("CatalogName2")
    .type(DataCatalogType2.HIVE)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



