# Data Catalog Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nVHlwZTE

The type of data catalog to create: <code>LAMBDA</code> for a federated catalog, <code>HIVE</code> for an external hive metastore, or <code>GLUE</code> for an Glue Data Catalog.


# Enum Type Name

`DataCatalogType1`


# Fields

| Name |
|  --- |
| `Lambda` |
| `Glue` |
| `Hive` |


# Example

```csharp
using AmazonAthena.Standard.Models;

DataCatalogType1 dataCatalogType1 = DataCatalogType1.Glue;
```



