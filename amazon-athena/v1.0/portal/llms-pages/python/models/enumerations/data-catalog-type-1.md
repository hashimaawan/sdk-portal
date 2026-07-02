# Data Catalog Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nVHlwZTE

The type of data catalog to create: <code>LAMBDA</code> for a federated catalog, <code>HIVE</code> for an external hive metastore, or <code>GLUE</code> for an Glue Data Catalog.


# Enum Type Name

`DataCatalogType1`


# Fields

| Name |
|  --- |
| `LAMBDA` |
| `GLUE` |
| `HIVE` |


# Example

```python
from amazonathena.models.data_catalog_type_1 import DataCatalogType1

data_catalog_type_1 = DataCatalogType1.GLUE
```



