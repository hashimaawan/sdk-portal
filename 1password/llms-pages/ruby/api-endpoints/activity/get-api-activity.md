# Get Api Activity

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRkFjdGl2aXR5JTJGR2V0QXBpQWN0aXZpdHk

```ruby
def get_api_activity(limit: 50,
                     offset: 0)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `Integer` | Query, Optional | How many API Events should be retrieved in a single request.<br><br>**Default**: `50` |
| `offset` | `Integer` | Query, Optional | How far into the collection of API Events should the response start<br><br>**Default**: `0` |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`Array[ApiRequest]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/api-request.md).


# Example Usage

```ruby
limit = 10

offset = 50

result = activity_api.get_api_activity(
  limit: limit,
  offset: offset
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |



