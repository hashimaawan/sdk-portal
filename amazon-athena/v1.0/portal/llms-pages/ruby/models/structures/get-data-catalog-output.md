# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data_catalog` | [`DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/data-catalog-2.md) | Optional | - |


# Example

```ruby
get_data_catalog_output = GetDataCatalogOutput.new(
  DataCatalog2.new(
    'Name4',
    DataCatalogType1Enum::GLUE,
    'Description2',
    Parameters.new
  )
)
```



