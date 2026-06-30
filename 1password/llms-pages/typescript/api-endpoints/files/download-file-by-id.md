# Download File by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0ZSUyRkZpbGVzJTJGRG93bmxvYWRGaWxlQnlJRA

```ts
async downloadFileById(
  vaultUuid: string,
  itemUuid: string,
  fileUuid: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<NodeJS.ReadableStream | Blob>>
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault the item is in |
| `itemUuid` | `string` | Template, Required | The UUID of the Item the File is in |
| `fileUuid` | `string` | Template, Required | UUID of the file to get content from |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type `NodeJS.ReadableStream | Blob`.


# Example Usage

```ts
const vaultUuid = '00002186-0000-0000-0000-000000000000';

const itemUuid = '0000141a-0000-0000-0000-000000000000';

const fileUuid = 'fileUuid2';

try {
  const response = await filesApi.downloadFileById(
    vaultUuid,
    itemUuid,
    fileUuid
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
| 404 | File not found | [`ErrorResponseError`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/exceptions/error-response.md) |



