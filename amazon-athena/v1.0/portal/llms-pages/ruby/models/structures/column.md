# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `type` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` |
| `comment` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` |


# Example

```ruby
column = Column.new(
  'Name6',
  'Type6',
  'Comment2'
)
```



