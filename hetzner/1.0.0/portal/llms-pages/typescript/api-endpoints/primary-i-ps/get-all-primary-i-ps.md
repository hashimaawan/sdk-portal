# Get All Primary I Ps

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQcyUyRkdldCUyNTIwYWxsJTI1MjBQcmltYXJ5JTI1MjBJUHM

Returns all Primary IP objects.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllPrimaryIPs(
  name?: string,
  labelSelector?: string,
  ip?: string,
  sort?: Sort2Enum,
  requestOptions?: RequestOptions
): Promise<ApiResponse<PrimaryIPsResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `labelSelector` | `string \| undefined` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `ip` | `string \| undefined` | Query, Optional | Can be used to filter resources by their ip. The response will only contain the resources matching the specified ip. |
| `sort` | [`Sort2Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/sort-2.md) | Query, Optional | Can be used multiple times. Choices id id:asc id:desc created created:asc created:desc |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `primary_ips` key contains an array of Primary IP objects

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`PrimaryIPsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/primary-i-ps-response.md).


# Example Usage

```ts
const ip = '127.0.0.1';

try {
  const response = await primaryIPsController.getAllPrimaryIPs(
    undefined,
    undefined,
    ip
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



