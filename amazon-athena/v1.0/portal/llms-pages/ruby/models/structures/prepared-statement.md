# Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50

A prepared SQL statement for use with Athena.


# Class Name

`PreparedStatement`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statement_name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `query_statement` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `work_group_name` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `last_modified_time` | `DateTime` | Optional | - |


# Example

```ruby
prepared_statement = PreparedStatement.new(
  'StatementName8',
  'QueryStatement2',
  'WorkGroupName2',
  'Description6',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z')
)
```



