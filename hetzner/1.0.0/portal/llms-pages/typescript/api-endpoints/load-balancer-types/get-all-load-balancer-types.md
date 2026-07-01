# Get All Load Balancer Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyRkdldCUyNTIwYWxsJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwVHlwZXM

Gets all Load Balancer type objects.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllLoadBalancerTypes(
  name?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<LoadBalancerTypesResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Query, Optional | Can be used to filter Load Balancer types by their name. The response will only contain the Load Balancer type matching the specified name. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `load_balancer_types` key in the reply contains an array of Load Balancer type objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`LoadBalancerTypesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-types-response.md).


# Example Usage

```ts
try {
  const response = await loadBalancerTypesApi.getAllLoadBalancerTypes();

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



