# Create Presigned Notebook Url Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJsUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`CreatePresignedNotebookUrlResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `notebook_url` | `String` | Required | - |
| `auth_token` | `String` | Required | **Constraints**: *Maximum Length*: `2048` |
| `auth_token_expiration_time` | `Integer` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_presigned_notebook_url_response = CreatePresignedNotebookUrlResponse.new(
  notebook_url: 'NotebookUrl8',
  auth_token: 'AuthToken2',
  auth_token_expiration_time: 54,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



