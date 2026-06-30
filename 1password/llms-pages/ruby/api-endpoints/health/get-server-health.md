# Get Server Health

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRkhlYWx0aCUyRkdldFNlcnZlckhlYWx0aA

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_server_health
```


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`HealthResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/health-response.md).


# Example Usage

```ruby
result = health_api.get_server_health

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "dependencies": [
    {
      "service": "sync",
      "status": "TOKEN_NEEDED"
    },
    {
      "message": "Connected to./1password.sqlite",
      "service": "sqlite",
      "status": "ACTIVE"
    }
  ],
  "name": "1Password Connect API",
  "version": "1.2.1"
}
```



