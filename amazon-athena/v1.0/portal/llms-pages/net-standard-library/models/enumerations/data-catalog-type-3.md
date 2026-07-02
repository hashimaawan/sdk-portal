# Data Catalog Type 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nVHlwZTM

Specifies the type of data catalog to update. Specify <code>LAMBDA</code> for a federated catalog, <code>HIVE</code> for an external hive metastore, or <code>GLUE</code> for an Glue Data Catalog.


# Enum Type Name

`DataCatalogType3`


# Fields

| Name |
|  --- |
| `Lambda` |
| `Glue` |
| `Hive` |


# Example

```csharp
using AmazonAthena.Standard.Models;

DataCatalogType3 dataCatalogType3 = DataCatalogType3.Lambda;
```



