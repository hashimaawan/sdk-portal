# Get Api Activity

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0ZSUyRkFjdGl2aXR5JTJGR2V0QXBpQWN0aXZpdHk

```ts
async getApiActivity(
  limit?: number,
  offset?: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ApiRequest[]>>
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `number \| undefined` | Query, Optional | How many API Events should be retrieved in a single request.<br><br>**Default**: `50` |
| `offset` | `number \| undefined` | Query, Optional | How far into the collection of API Events should the response start<br><br>**Default**: `0` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`ApiRequest[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/api-request.md).


# Example Usage

```ts
const limit = 10;

const offset = 50;

try {
  const response = await activityApi.getApiActivity(
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
    if (error instanceof ErrorResponseError) {
      console.log(error.result);
    }
  }
}
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseError`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/exceptions/error-response.md) |



