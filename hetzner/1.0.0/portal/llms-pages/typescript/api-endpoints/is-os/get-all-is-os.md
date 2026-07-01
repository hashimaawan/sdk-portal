# Get All IS Os

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRklTT3MlMkZHZXQlMjUyMGFsbCUyNTIwSVNPcw

Returns all available ISO objects.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllIsOs(
  name?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<IsosResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Query, Optional | Can be used to filter ISOs by their name. The response will only contain the ISO matching the specified name. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `isos` key in the reply contains an array of iso objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`IsosResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/isos-response.md).


# Example Usage

```ts
try {
  const response = await isOsApi.getAllIsOs();

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



