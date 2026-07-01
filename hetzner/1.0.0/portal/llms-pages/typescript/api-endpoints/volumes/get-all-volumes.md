# Get All Volumes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZHZXQlMjUyMGFsbCUyNTIwVm9sdW1lcw

Gets all existing Volumes that you have available.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllVolumes(
  status?: Status23,
  sort?: Sort,
  name?: string,
  labelSelector?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<VolumesResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status23 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/status-23.md) | Query, Optional | Can be used multiple times. The response will only contain Volumes matching the status. |
| `sort` | [`Sort \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/sort.md) | Query, Optional | Can be used multiple times. |
| `name` | `string \| undefined` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `string \| undefined` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `volumes` key contains a list of volumes

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`VolumesResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/volumes-response.md).


# Example Usage

```ts
try {
  const response = await volumesApi.getAllVolumes();

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



