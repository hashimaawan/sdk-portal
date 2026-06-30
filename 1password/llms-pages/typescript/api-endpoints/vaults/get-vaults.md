# Get Vaults

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0ZSUyRlZhdWx0cyUyRkdldFZhdWx0cw

```ts
async getVaults(
  filter?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<Vault[]>>
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | `string \| undefined` | Query, Optional | Filter the Vault collection based on Vault name using SCIM eq filter |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`Vault[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/vault.md).


# Example Usage

```ts
const filter = 'name eq "Some Vault Name"';

try {
  const response = await vaultsApi.getVaults(filter);

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



