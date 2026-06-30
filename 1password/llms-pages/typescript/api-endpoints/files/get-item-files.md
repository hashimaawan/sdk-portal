# Get Item Files

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0ZSUyRkZpbGVzJTJGR2V0SXRlbUZpbGVz

```ts
async getItemFiles(
  vaultUuid: string,
  itemUuid: string,
  inlineFiles?: boolean,
  requestOptions?: RequestOptions
): Promise<ApiResponse<File[]>>
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault to fetch Items from |
| `itemUuid` | `string` | Template, Required | The UUID of the Item to fetch files from |
| `inlineFiles` | `boolean \| undefined` | Query, Optional | Tells server to return the base64-encoded file contents in the response. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`File[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/file.md).


# Example Usage

```ts
const vaultUuid = '00002186-0000-0000-0000-000000000000';

const itemUuid = '0000141a-0000-0000-0000-000000000000';

const inlineFiles = true;

try {
  const response = await filesApi.getItemFiles(
    vaultUuid,
    itemUuid,
    inlineFiles
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
| 404 | Item not found | [`ErrorResponseError`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/exceptions/error-response.md) |
| 413 | File content too large to display | [`ErrorResponseError`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/exceptions/error-response.md) |



