# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFiYXNl

Contains metadata information for a database in a data catalog.

*This model accepts additional fields of type Object.*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/parameters.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
database = Database.new(
  name: 'Name0',
  description: 'Description6',
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



