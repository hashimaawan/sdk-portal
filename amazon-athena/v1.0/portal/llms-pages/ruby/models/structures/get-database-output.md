# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | [`Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/database-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_database_output = GetDatabaseOutput.new(
  database: Database2.new(
    name: 'Name2',
    description: 'Description8',
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



