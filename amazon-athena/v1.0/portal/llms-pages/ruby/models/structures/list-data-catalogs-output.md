# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data_catalogs_summary` | [`Array[DataCatalogSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/data-catalog-summary.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_data_catalogs_output = ListDataCatalogsOutput.new(
  data_catalogs_summary: [
    DataCatalogSummary.new(
      catalog_name: 'CatalogName4',
      type: DataCatalogType2::HIVE,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    DataCatalogSummary.new(
      catalog_name: 'CatalogName4',
      type: DataCatalogType2::HIVE,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    DataCatalogSummary.new(
      catalog_name: 'CatalogName4',
      type: DataCatalogType2::HIVE,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  next_token: 'NextToken2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



