# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `table_metadata_list` | [`Array[TableMetadata]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/table-metadata.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ruby
list_table_metadata_output = ListTableMetadataOutput.new(
  [
    TableMetadata.new(
      'Name2',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      'TableType2',
      [
        Column.new(
          'Name0',
          'Type0',
          'Comment4'
        )
      ],
      [
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        ),
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        ),
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        )
      ],
      Parameters.new
    ),
    TableMetadata.new(
      'Name2',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      'TableType2',
      [
        Column.new(
          'Name0',
          'Type0',
          'Comment4'
        )
      ],
      [
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        ),
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        ),
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        )
      ],
      Parameters.new
    ),
    TableMetadata.new(
      'Name2',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      'TableType2',
      [
        Column.new(
          'Name0',
          'Type0',
          'Comment4'
        )
      ],
      [
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        ),
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        ),
        Column.new(
          'Name6',
          'Type6',
          'Comment0'
        )
      ],
      Parameters.new
    )
  ],
  'NextToken8'
)
```



