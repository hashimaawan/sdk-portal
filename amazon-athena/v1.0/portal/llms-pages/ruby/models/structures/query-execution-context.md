# Query Execution Context

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dA

The database and data catalog context in which the query execution occurs.

*This model accepts additional fields of type Object.*


# Class Name

`QueryExecutionContext`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `catalog` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
query_execution_context = QueryExecutionContext.new(
  database: 'Database4',
  catalog: 'Catalog0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



