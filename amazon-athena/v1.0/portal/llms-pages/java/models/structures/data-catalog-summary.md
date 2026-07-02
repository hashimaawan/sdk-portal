# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CatalogName` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | String getCatalogName() | setCatalogName(String catalogName) |
| `Type` | [`DataCatalogType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/java/models/enumerations/data-catalog-type-2.md) | Optional | - | DataCatalogType2Enum getType() | setType(DataCatalogType2Enum type) |


# Example

```java
import com.amazonaws.useast1.athena.models.DataCatalogSummary;
import com.amazonaws.useast1.athena.models.DataCatalogType2Enum;

DataCatalogSummary dataCatalogSummary = new DataCatalogSummary.Builder()
    .catalogName("CatalogName2")
    .type(DataCatalogType2Enum.HIVE)
    .build();
```



