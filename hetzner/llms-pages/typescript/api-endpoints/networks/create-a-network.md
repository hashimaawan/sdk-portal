# Create a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGQ3JlYXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Creates a network with the specified `ip_range`.

You may specify one or more `subnets`. You can also add more Subnets later by using the [add subnet action](https://docs.hetzner.cloud/#network-actions-add-a-subnet-to-a-network). If you do not specify an `ip_range` in the subnet we will automatically pick the first available /24 range for you.

You may specify one or more routes in `routes`. You can also add more routes later by using the [add route action](https://docs.hetzner.cloud/#network-actions-add-a-route-to-a-network).

:information_source: **Note** This endpoint does not require authentication.

```ts
async createANetwork(
  body?: CreateNetworkRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<NetworksResponse1>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`CreateNetworkRequest \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/create-network-request.md) | Body, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**201**: The `network` key contains the network that was just created

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`NetworksResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/networks-response-1.md).


# Example Usage

```ts
const body: CreateNetworkRequest = {
  ipRange: '10.0.0.0/16',
  name: 'mynet',
};

try {
  const response = await networksController.createANetwork(body);

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



