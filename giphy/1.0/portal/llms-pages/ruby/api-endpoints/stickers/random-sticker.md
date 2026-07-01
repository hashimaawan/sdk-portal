# Random Sticker

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGcmFuZG9tU3RpY2tlcg

Returns a random GIF, limited by tag. Excluding the tag parameter will return a random GIF from the GIPHY catalog.

```ruby
def random_sticker(tag: nil,
                   rating: nil)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tag` | `String` | Query, Optional | Filters results by specified tag. |
| `rating` | `String` | Query, Optional | Filters results by specified rating. |


# Response Type

**200**

[`StickersRandomResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/stickers-random-response.md)


# Example Usage

```ruby
result = stickers_controller.random_sticker
puts result
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `APIException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `APIException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `APIException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `APIException` |



