# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_metadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/notebook-metadata-1.md) | Optional | - |
| `payload` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
export_notebook_output = ExportNotebookOutput.new(
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
  payload: 'Payload6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



