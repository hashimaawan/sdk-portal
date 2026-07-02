# Data Catalog Type 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nVHlwZTM

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

```python
from amazonathena.models.data_catalog_type_3_enum import DataCatalogType3Enum

data_catalog_type_3 = DataCatalogType3Enum.GLUE
```



