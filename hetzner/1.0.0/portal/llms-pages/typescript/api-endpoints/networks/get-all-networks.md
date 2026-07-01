# Get All Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGR2V0JTI1MjBhbGwlMjUyME5ldHdvcmtz

Gets all existing networks that you have available.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllNetworks(
  name?: string,
  labelSelector?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<NetworksResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Query, Optional | Can be used to filter networks by their name. The response will only contain the networks matching the specified name. |
| `labelSelector` | `string \| undefined` | Query, Optional | Can be used to filter networks by labels. The response will only contain networks with a matching label selector pattern. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `networks` key contains a list of networks

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`NetworksResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/networks-response.md).


# Example Usage

```ts
try {
  const response = await networksApi.getAllNetworks();

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



