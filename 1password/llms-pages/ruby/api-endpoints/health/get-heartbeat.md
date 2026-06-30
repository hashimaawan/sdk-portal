# Get Heartbeat

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldEhlYXJ0YmVhdA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_heartbeat
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type `String`.


# Example Usage

```ruby
result = health_api.get_heartbeat

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```



