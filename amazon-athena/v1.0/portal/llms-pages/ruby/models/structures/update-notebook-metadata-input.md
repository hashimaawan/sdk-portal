# Update Notebook Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rTWV0YWRhdGFJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`UpdateNotebookMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_notebook_metadata_input = UpdateNotebookMetadataInput.new(
  notebook_id: 'NotebookId0',
  name: 'Name0',
  client_request_token: 'ClientRequestToken4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



