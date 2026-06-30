# Transfer-a-Users-Playback

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0ZSUyRlBsYXllciUyRnRyYW5zZmVyLWEtdXNlcnMtcGxheWJhY2s

Transfer playback to a new device and optionally begin playback. This API only works for users who have Spotify Premium. The order of execution is not guaranteed when you use this API with other Player API endpoints.

```ts
async transferAUsersPlayback(
  body?: MePlayerRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Authentication

This endpoint requires [oauth_2_0](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`MePlayerRequest \| undefined`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/me-player-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Requires scope

## oauth_2_0

`user-modify-playback-state`


# Response Type

**204**: Playback transferred

This method returns an [`ApiResponse`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const body: MePlayerRequest = {
  deviceIds: [
    '74ASZWbe4lXaubB36ztrGX'
  ],
};

try {
  const response = await playerApi.transferAUsersPlayback(body);

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
    if (error instanceof UnauthorizedError) {
      console.log(error.result);
    } else if (error instanceof ForbiddenError) {
      console.log(error.result);
    } else if (error instanceof TooManyRequestsError) {
      console.log(error.result);
    }
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Bad or expired token. This can happen if the user revoked a token or<br>the access token has expired. You should re-authenticate the user. | [`UnauthorizedError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/exceptions/unauthorized.md) |
| 403 | Bad OAuth request (wrong consumer key, bad nonce, expired<br>timestamp...). Unfortunately, re-authenticating the user won't help here. | [`ForbiddenError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/exceptions/forbidden.md) |
| 429 | The app has exceeded its rate limits. | [`TooManyRequestsError`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/exceptions/too-many-requests.md) |



