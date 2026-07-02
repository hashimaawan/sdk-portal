# Data Catalog Type 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nVHlwZTM

Specifies the type of data catalog to update. Specify <code>LAMBDA</code> for a federated catalog, <code>HIVE</code> for an external hive metastore, or <code>GLUE</code> for an Glue Data Catalog.


# Enum Type Name

`DataCatalogType3Enum`


# Fields

| Name |
|  --- |
| `LAMBDA` |
| `GLUE` |
| `HIVE` |


# Example

```java
import com.amazonaws.useast1.athena.models.DataCatalogType3Enum;

DataCatalogType3Enum dataCatalogType3 = DataCatalogType3Enum.LAMBDA;
```



