# Export Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ExportNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
export_notebook_input = ExportNotebookInput.new(
  notebook_id: 'NotebookId0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



