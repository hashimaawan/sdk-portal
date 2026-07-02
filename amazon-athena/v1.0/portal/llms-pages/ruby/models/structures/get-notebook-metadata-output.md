# Get Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFPdXRwdXQ

*This model accepts additional fields of type Object.*


# Class Name

`GetNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_metadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/notebook-metadata-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_notebook_metadata_output = GetNotebookMetadataOutput.new(
  notebook_metadata: NotebookMetadata1.new(
    notebook_id: 'NotebookId0',
    name: 'Name0',
    work_group: 'WorkGroup2',
    creation_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    type: NotebookType1::IPYNB,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



