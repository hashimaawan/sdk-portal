# Get All SSH Keys

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkdldCUyNTIwYWxsJTI1MjBTU0glMjUyMGtleXM

Returns all SSH key objects.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getAllSshKeys(
  sort?: Sort8,
  name?: string,
  fingerprint?: string,
  labelSelector?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SshKeysResponse>>
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort` | [`Sort8 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/sort-8.md) | Query, Optional | Can be used multiple times. |
| `name` | `string \| undefined` | Query, Optional | Can be used to filter resources by their name. The response will only contain the resources matching the specified name |
| `fingerprint` | `string \| undefined` | Query, Optional | Can be used to filter SSH keys by their fingerprint. The response will only contain the SSH key matching the specified fingerprint. |
| `labelSelector` | `string \| undefined` | Query, Optional | Can be used to filter resources by labels. The response will only contain resources matching the label selector. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: The `ssh_keys` key in the reply contains an array of SSH key objects with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type [`SshKeysResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ssh-keys-response.md).


# Example Usage

```ts
try {
  const response = await sshKeysApi.getAllSshKeys();

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



