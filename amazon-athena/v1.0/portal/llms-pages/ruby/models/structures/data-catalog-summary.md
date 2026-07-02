# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.

*This model accepts additional fields of type Object.*


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `type` | [`DataCatalogType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/data-catalog-type-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
data_catalog_summary = DataCatalogSummary.new(
  catalog_name: 'CatalogName4',
  type: DataCatalogType2::HIVE,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



