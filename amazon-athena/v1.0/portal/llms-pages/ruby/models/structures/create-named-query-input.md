# Create Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type Object.*


# Class Name

`CreateNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `database` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `query_string` | `String` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `work_group` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_named_query_input = CreateNamedQueryInput.new(
  name: 'Name0',
  database: 'Database8',
  query_string: 'QueryString2',
  description: 'Description6',
  client_request_token: 'ClientRequestToken4',
  work_group: 'WorkGroup2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



