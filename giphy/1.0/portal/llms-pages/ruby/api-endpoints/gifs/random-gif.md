# Random Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0ZSUyRmdpZnMlMkZyYW5kb21HaWY

Returns a random GIF, limited by tag. Excluding the tag parameter will return a random GIF from the GIPHY catalog.

```ruby
def random_gif(tag: nil,
               rating: nil)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tag` | `String` | Query, Optional | Filters results by specified tag. |
| `rating` | `String` | Query, Optional | Filters results by specified rating. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`GifsRandomResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/gifs-random-response.md).


# Example Usage

```ruby
result = gifs_api.random_gif

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `APIException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `APIException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `APIException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `APIException` |



