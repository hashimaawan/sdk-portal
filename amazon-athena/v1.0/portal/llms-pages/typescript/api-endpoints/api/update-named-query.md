# Update Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0ZSUyRiUyRlVwZGF0ZU5hbWVkUXVlcnk

Updates a <a>NamedQuery</a> object. The database or workgroup cannot be updated.

```ts
async updateNamedQuery(
  xAmzTarget: XAmzTarget55,
  body: UpdateNamedQueryInput,
  xAmzContentSha256?: string,
  xAmzDate?: string,
  xAmzAlgorithm?: string,
  xAmzCredential?: string,
  xAmzSecurityToken?: string,
  xAmzSignature?: string,
  xAmzSignedHeaders?: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<unknown | undefined>>
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `xAmzTarget` | [`XAmzTarget55`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/x-amz-target-55.md) | Header, Required | - |
| `body` | [`UpdateNamedQueryInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/update-named-query-input.md) | Body, Required | - |
| `xAmzContentSha256` | `string \| undefined` | Header, Optional | - |
| `xAmzDate` | `string \| undefined` | Header, Optional | - |
| `xAmzAlgorithm` | `string \| undefined` | Header, Optional | - |
| `xAmzCredential` | `string \| undefined` | Header, Optional | - |
| `xAmzSecurityToken` | `string \| undefined` | Header, Optional | - |
| `xAmzSignature` | `string \| undefined` | Header, Optional | - |
| `xAmzSignedHeaders` | `string \| undefined` | Header, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/sdk-infrastructure/utilities/apiresponse.md) instance. The `result` property of this instance returns the response data which is of type `unknown`.


# Example Usage

```ts
const xAmzTarget = XAmzTarget55.EnumAmazonAthenaUpdateNamedQuery;

const body: UpdateNamedQueryInput = {
  namedQueryId: 'NamedQueryId6',
  name: 'Name6',
  queryString: 'QueryString8',
};

try {
  const response = await api.updateNamedQuery(
    xAmzTarget,
    body
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


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiError` |
| 481 | InvalidRequestException | `ApiError` |



