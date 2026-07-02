# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `notebook_metadata_list` | [`Array[NotebookMetadata]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/notebook-metadata.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_notebook_metadata_output = ListNotebookMetadataOutput.new(
  next_token: 'NextToken8',
  notebook_metadata_list: [
    NotebookMetadata.new(
      notebook_id: 'NotebookId4',
      name: 'Name4',
      work_group: 'WorkGroup6',
      creation_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      type: NotebookType1::IPYNB,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



