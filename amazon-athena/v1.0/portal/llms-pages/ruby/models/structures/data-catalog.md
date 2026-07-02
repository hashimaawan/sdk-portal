# Data Catalog

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9n

<p>Contains information about a data catalog in an Amazon Web Services account.</p> <note> <p>In the Athena console, data catalogs are listed as "data sources" on the <b>Data sources</b> page under the <b>Data source name</b> column.</p> </note>
*This model accepts additional fields of type Object.*


# Class Name

`DataCatalog`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `type` | [`DataCatalogType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/data-catalog-type-1.md) | Required | - |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/parameters.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
data_catalog = DataCatalog.new(
  name: 'Name8',
  type: DataCatalogType1::LAMBDA,
  description: 'Description8',
  parameters: Parameters.new(
    additional_properties: {
      'exampleAdditionalProperty' => 'Parameters_additionalProperties2'
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



