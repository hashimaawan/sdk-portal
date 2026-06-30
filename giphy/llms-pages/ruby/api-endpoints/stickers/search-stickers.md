# Search Stickers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/ruby/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGc2VhcmNoU3RpY2tlcnM

Replicates the functionality and requirements of the classic GIPHY search, but returns animated stickers rather than GIFs.

```ruby
def search_stickers(q,
                    limit: 25,
                    offset: 0,
                    rating: nil,
                    lang: nil)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `String` | Query, Required | Search query term or prhase. |
| `limit` | `Integer` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `Integer` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `String` | Query, Optional | Filters results by specified rating. |
| `lang` | `String` | Query, Optional | Specify default language for regional content; use a 2-letter ISO 639-1 language code. |


# Response Type

**200**: Search results

[`StickersSearchResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/stickers-search-response.md)


# Example Usage

```ruby
q = 'q0'

limit = 25

offset = 0

result = stickers_controller.search_stickers(
  q,
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



