# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `table_metadata` | [`TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/table-metadata-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_table_metadata_output = GetTableMetadataOutput.new(
  table_metadata: TableMetadata2.new(
    name: 'Name6',
    create_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    last_access_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    table_type: 'TableType0',
    columns: [
      Column.new(
        name: 'Name0',
        type: 'Type0',
        comment: 'Comment4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Column.new(
        name: 'Name0',
        type: 'Type0',
        comment: 'Comment4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
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
      )
    ],
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



