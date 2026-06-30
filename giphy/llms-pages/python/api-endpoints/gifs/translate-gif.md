# Translate Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/python/x-redirect/JTI0ZSUyRmdpZnMlMkZ0cmFuc2xhdGVHaWY

The translate API draws on search, but uses the GIPHY `special sauce` to handle translating from one vocabulary to another. In this case, words and phrases to GIF

```python
def translate_gif(self,
                 s)
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `s` | `str` | Query, Required | Search term. |


# Response Type

**200**

[`GifsTranslateResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/python/models/structures/gifs-translate-response.md)


# Example Usage

```python
s = 's8'

result = gifs_controller.translate_gif(s)
print(result)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `APIException` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `APIException` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `APIException` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `APIException` |



