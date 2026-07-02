# Get Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_metadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/notebook-metadata-1.md) | Optional | - |


# Example

```ruby
get_notebook_metadata_output = GetNotebookMetadataOutput.new(
  NotebookMetadata1.new(
    'NotebookId0',
    'Name0',
    'WorkGroup2',
    DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
    NotebookType1Enum::IPYNB,
    DateTimeHelper.from_rfc3339(nil)
  )
)
```



