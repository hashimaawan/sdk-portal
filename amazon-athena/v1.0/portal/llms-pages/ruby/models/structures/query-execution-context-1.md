# Query Execution Context 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dDE

*This model accepts additional fields of type Object.*


# Class Name

`QueryExecutionContext1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `catalog` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
query_execution_context1 = QueryExecutionContext1.new(
  database: 'Database2',
  catalog: 'Catalog8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



