# Query Execution Context 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dDE


# Class Name

`QueryExecutionContext1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `catalog` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |


# Example

```ruby
query_execution_context1 = QueryExecutionContext1.new(
  'Database2',
  'Catalog8'
)
```



