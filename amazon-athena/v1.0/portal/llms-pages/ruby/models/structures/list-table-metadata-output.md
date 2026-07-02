# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `table_metadata_list` | [`Array[TableMetadata]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/table-metadata.md) | Optional | - |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_table_metadata_output = ListTableMetadataOutput.new(
  table_metadata_list: [
    TableMetadata.new(
      name: 'Name2',
      create_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      last_access_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      table_type: 'TableType2',
      columns: [
        Column.new(
          name: 'Name0',
          type: 'Type0',
          comment: 'Comment4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      partition_keys: [
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    TableMetadata.new(
      name: 'Name2',
      create_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      last_access_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      table_type: 'TableType2',
      columns: [
        Column.new(
          name: 'Name0',
          type: 'Type0',
          comment: 'Comment4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      partition_keys: [
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    TableMetadata.new(
      name: 'Name2',
      create_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      last_access_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      table_type: 'TableType2',
      columns: [
        Column.new(
          name: 'Name0',
          type: 'Type0',
          comment: 'Comment4',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      partition_keys: [
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Column.new(
          name: 'Name6',
          type: 'Type6',
          comment: 'Comment0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  next_token: 'NextToken8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



