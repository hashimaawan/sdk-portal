# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_metadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/notebook-metadata-1.md) | Optional | - |
| `payload` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |


# Example

```ruby
export_notebook_output = ExportNotebookOutput.new(
  NotebookMetadata1.new(
    'NotebookId0',
    'Name0',
    'WorkGroup2',
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    NotebookType1Enum::IPYNB,
    DateTimeHelper.from_rfc3339(nil)
  ),
  'Payload6'
)
```



