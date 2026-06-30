# Delete Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0ZSUyRkl0ZW1zJTJGRGVsZXRlVmF1bHRJdGVt

```ts
async deleteVaultItem(
  vaultUuid: string,
  itemUuid: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vaultUuid` | `string` | Template, Required | The UUID of the Vault the item is in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `itemUuid` | `string` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**204**: Successfully deleted an item

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```ts
const vaultUuid = 'vaultUuid2';

const itemUuid = 'itemUuid6';

try {
  const response = await itemsApi.deleteVaultItem(
    vaultUuid,
    itemUuid
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
| 403 | Unauthorized access | [`ErrorResponseError`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseError`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/exceptions/error-response.md) |



