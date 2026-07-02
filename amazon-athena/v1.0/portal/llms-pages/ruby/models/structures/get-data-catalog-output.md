# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data_catalog` | [`DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/data-catalog-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_data_catalog_output = GetDataCatalogOutput.new(
  data_catalog: DataCatalog2.new(
    name: 'Name4',
    type: DataCatalogType1::GLUE,
    description: 'Description2',
    parameters: Parameters.new(
      additional_properties: {
        'exampleAdditionalProperty' => 'Parameters_additionalProperties2'
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



