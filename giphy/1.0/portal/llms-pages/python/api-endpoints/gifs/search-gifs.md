# Search Gifs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/python/x-redirect/JTI0ZSUyRmdpZnMlMkZzZWFyY2hHaWZz

Search all GIPHY GIFs for a word or phrase. Punctuation will be stripped and ignored.  Use a plus or url encode for phrases. Example paul+rudd, ryan+gosling or american+psycho.

```python
def search_gifs(self,
               q,
               limit=25,
               offset=0,
               rating=None,
               lang=None)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `q` | `str` | Query, Required | Search query term or prhase. |
| `limit` | `int` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `int` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `str` | Query, Optional | Filters results by specified rating. |
| `lang` | `str` | Query, Optional | Specify default language for regional content; use a 2-letter ISO 639-1 language code. |


# Response Type

**200**: Search results

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`GifsSearchResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/gifs-search-response.md).


# Example Usage

```python
q = 'q0'

limit = 25

offset = 0

result = gifs_api.search_gifs(
    q,
    limit=limit,
    offset=offset
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `ApiException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `ApiException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `ApiException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `ApiException` |



