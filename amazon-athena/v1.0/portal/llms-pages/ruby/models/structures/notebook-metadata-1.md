# Notebook Metadata 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGEx

*This model accepts additional fields of type Object.*


# Class Name

`NotebookMetadata1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `name` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `creation_time` | `DateTime` | Optional | - |
| `type` | [`NotebookType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/notebook-type-1.md) | Optional | - |
| `last_modified_time` | `DateTime` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
notebook_metadata1 = NotebookMetadata1.new(
  notebook_id: 'NotebookId0',
  name: 'Name0',
  work_group: 'WorkGroup2',
  creation_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  type: NotebookType1::IPYNB,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



