# Result Set 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFNldDI


# Class Name

`ResultSet2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rows` | [`Array[Row]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/row.md) | Optional | - |
| `result_set_metadata` | [`ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-set-metadata-2.md) | Optional | - |


# Example

```ruby
result_set2 = ResultSet2.new(
  [
    Row.new(
      [
        Datum.new(
          'VarCharValue8'
        ),
        Datum.new(
          'VarCharValue8'
        )
      ]
    ),
    Row.new(
      [
        Datum.new(
          'VarCharValue8'
        ),
        Datum.new(
          'VarCharValue8'
        )
      ]
    )
  ],
  ResultSetMetadata2.new(
    [
      ColumnInfo.new(
        'Name6',
        'Type6',
        'CatalogName0',
        'SchemaName0',
        'TableName2',
        'Label4',
        48,
        nil,
        envrr
      )
    ]
  )
)
```



