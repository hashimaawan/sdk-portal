# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database_list` | [`Array[Database]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/database.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_databases_output = ListDatabasesOutput.new(
  database_list: [
    Database.new(
      name: 'Name4',
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
  ],
  next_token: 'NextToken8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



