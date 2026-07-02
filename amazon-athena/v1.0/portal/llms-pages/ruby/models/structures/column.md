# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.

*This model accepts additional fields of type Object.*


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `type` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` |
| `comment` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
column = Column.new(
  name: 'Name6',
  type: 'Type6',
  comment: 'Comment2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



