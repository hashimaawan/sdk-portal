# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `table_metadata` | [`TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/table-metadata-2.md) | Optional | - |


# Example

```ruby
get_table_metadata_output = GetTableMetadataOutput.new(
  TableMetadata2.new(
    'Name6',
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    'TableType0',
    [
      Column.new(
        'Name0',
        'Type0',
        'Comment4'
      ),
      Column.new(
        'Name0',
        'Type0',
        'Comment4'
      ),
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
      )
    ],
    Parameters.new
  )
)
```



