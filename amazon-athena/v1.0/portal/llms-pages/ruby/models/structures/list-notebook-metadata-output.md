# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0


# Class Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `notebook_metadata_list` | [`Array[NotebookMetadata]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/notebook-metadata.md) | Optional | - |


# Example

```ruby
list_notebook_metadata_output = ListNotebookMetadataOutput.new(
  'NextToken8',
  [
    NotebookMetadata.new(
      'NotebookId4',
      'Name4',
      'WorkGroup6',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      NotebookType1Enum::IPYNB,
      DateTimeHelper.from_rfc3339(nil)
    )
  ]
)
```



