# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `payload` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `type` | [`NotebookType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/notebook-type-2.md) | Required | - |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
import_notebook_input = ImportNotebookInput.new(
  work_group: 'WorkGroup8',
  name: 'Name6',
  payload: 'Payload2',
  type: NotebookType2::IPYNB,
  client_request_token: 'ClientRequestToken0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



