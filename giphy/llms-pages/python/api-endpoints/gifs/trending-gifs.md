# Trending Gifs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/python/x-redirect/JTI0ZSUyRmdpZnMlMkZ0cmVuZGluZ0dpZnM

Fetch GIFs currently trending online. Hand curated by the GIPHY editorial team.  The data returned mirrors the GIFs showcased on the GIPHY homepage. Returns 25 results by default.

```python
def trending_gifs(self,
                 limit=25,
                 offset=0,
                 rating=None)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `int` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `int` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `str` | Query, Optional | Filters results by specified rating. |


# Response Type

**200**

[`GifsTrendingResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/gifs-trending-response.md)


# Example Usage

```python
limit = 25

offset = 0

result = gifs_controller.trending_gifs(
    limit=limit,
    offset=offset
)
print(result)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `APIException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `APIException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `APIException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `APIException` |



