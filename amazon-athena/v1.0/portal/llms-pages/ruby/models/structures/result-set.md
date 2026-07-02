# Result Set

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlJlc3VsdFNldA

The metadata and rows that make up a query result set. The metadata describes the column structure and data types. To return a <code>ResultSet</code> object, use <a>GetQueryResults</a>.


# Class Name

`ResultSet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rows` | [`Array[Row]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/row.md) | Optional | - |
| `result_set_metadata` | [`ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/result-set-metadata-2.md) | Optional | - |


# Example

```ruby
result_set = ResultSet.new(
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



