# Update Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlVwZGF0ZU5vdGVib29rSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`UpdateNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_id` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `payload` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `type` | [`NotebookType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/notebook-type-2.md) | Required | - |
| `session_id` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
update_notebook_input = UpdateNotebookInput.new(
  notebook_id: 'NotebookId6',
  payload: 'Payload2',
  type: NotebookType2::IPYNB,
  session_id: 'SessionId2',
  client_request_token: 'ClientRequestToken0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



