# Create Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZU5vdGVib29rSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`CreateNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_notebook_input = CreateNotebookInput.new(
  work_group: 'WorkGroup4',
  name: 'Name2',
  client_request_token: 'ClientRequestToken6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



