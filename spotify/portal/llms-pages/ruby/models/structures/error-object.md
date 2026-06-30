# Error Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRkVycm9yT2JqZWN0

*This model accepts additional fields of type Object.*


# Class Name

`ErrorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | `Integer` | Required | The HTTP status code (also returned in the response header; see [Response Status Codes](/documentation/web-api/concepts/api-calls#response-status-codes) for more information).<br><br>**Constraints**: `>= 400`, `<= 599` |
| `message` | `String` | Required | A short description of the cause of the error. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
error_object = ErrorObject.new(
  status: 400,
  message: 'message0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



