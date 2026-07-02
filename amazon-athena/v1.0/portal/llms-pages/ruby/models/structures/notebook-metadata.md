# Notebook Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGE

Contains metadata for notebook, including the notebook name, ID, workgroup, and time created.


# Class Name

`NotebookMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `creation_time` | `DateTime` | Optional | - |
| `type` | [`NotebookType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/notebook-type-1.md) | Optional | - |
| `last_modified_time` | `DateTime` | Optional | - |


# Example

```ruby
notebook_metadata = NotebookMetadata.new(
  'NotebookId4',
  'Name4',
  'WorkGroup6',
  DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  NotebookType1Enum::IPYNB,
  DateTimeHelper.from_rfc3339(nil)
)
```



