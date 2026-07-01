# Trending Stickers

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/typescript/x-redirect/JTI0ZSUyRnN0aWNrZXJzJTJGdHJlbmRpbmdTdGlja2Vycw

Fetch Stickers currently trending online. Hand curated by the GIPHY editorial team. Returns 25 results by default.

```ts
async trendingStickers(
  limit?: number,
  offset?: number,
  rating?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<StickersTrendingResponse>>
```


# Authentication

This endpoint requires [api_key](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/getting-started/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `number \| undefined` | Query, Optional | The maximum number of records to return.<br><br>**Default**: `25` |
| `offset` | `number \| undefined` | Query, Optional | An optional results offset.<br><br>**Default**: `0` |
| `rating` | `string \| undefined` | Query, Optional | Filters results by specified rating. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`StickersTrendingResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/typescript/models/structures/stickers-trending-response.md).


# Example Usage

```ts
const limit = 25;

const offset = 0;

try {
  const response = await stickersController.trendingStickers(
    limit,
    offset
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Your request was formatted incorrectly or missing required parameters. | `ApiError` |
| 403 | You weren't authorized to make your request; most likely this indicates an issue with your API Key. | `ApiError` |
| 404 | The particular GIF you are requesting was not found. This occurs, for example, if you request a GIF by an id that does not exist. | `ApiError` |
| 429 | Your API Key is making too many requests. Read about [requesting a Production Key](https://developers.giphy.com/docs/#access) to upgrade your API Key rate limits. | `ApiError` |



