# Delete a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZEZWxldGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Deletes a Floating IP. If it is currently assigned to a Server it will automatically get unassigned.

:information_source: **Note** This endpoint does not require authentication.

```ts
async deleteAFloatingIp(
  id: number,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Template, Required | ID of the Floating IP |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**204**: Floating IP deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const id = 112;

try {
  const response = await floatingIPsApi.deleteAFloatingIp(id);

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



