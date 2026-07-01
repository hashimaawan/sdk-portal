# Trending Stickers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGdHJlbmRpbmdTdGlja2Vycw

Fetch Stickers currently trending online. Hand curated by the GIPHY editorial team. Returns 25 results by default.

```ruby
def trending_stickers(limit: 25,
                      offset: 0,
                      rating: nil)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `Integer` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `Integer` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `String` | Query, Optional | Filters results by specified rating. |


# Response Type

**200**

[`StickersTrendingResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/stickers-trending-response.md)


# Example Usage

```ruby
limit = 25

offset = 0

result = stickers_controller.trending_stickers(
  limit: limit,
  offset: offset
)
puts result
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `APIException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `APIException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `APIException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `APIException` |



