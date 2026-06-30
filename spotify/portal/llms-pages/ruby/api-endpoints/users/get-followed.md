# Get-Followed

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0ZSUyRlVzZXJzJTJGZ2V0LWZvbGxvd2Vk

Get the current user's followed artists.

```ruby
def get_followed(type,
                 after: nil,
                 limit: 20)
```


# Authentication

This endpoint requires [oauth_2_0](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`ItemType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/enumerations/item-type-1.md) | Query, Required | - |
| `after` | `String` | Query, Optional | - |
| `limit` | `Integer` | Query, Optional | **Default**: `20`<br><br>**Constraints**: `>= 1`, `<= 50` |


# Requires scope

## oauth_2_0

`user-follow-read`


# Response Type

**200**: A paged set of artists

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`CursorPagedArtists`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/structures/cursor-paged-artists.md).


# Example Usage

```ruby
type = ItemType1::ARTIST

after = '0I2XqVXqHScXjHhk6AYYRe'

limit = 10

result = users_api.get_followed(
  type,
  after: after,
  limit: limit
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
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/ruby/models/exceptions/too-many-requests.md) |



