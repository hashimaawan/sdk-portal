# Get Gif by Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/python/x-redirect/JTI0ZSUyRmdpZnMlMkZnZXRHaWZCeUlk

Returns a GIF given that GIF's unique ID

```python
def get_gif_by_id(self,
                 gif_id)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gif_id` | `int` | Template, Required | Filters results by specified GIF ID. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`GifsResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/gifs-response-1.md).


# Example Usage

```python
gif_id = 250

result = gifs_api.get_gif_by_id(gif_id)

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



